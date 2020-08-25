**Paper title:**

Towards Memory Friendly Long-Short Term Memory Networks (LSTMs) on Mobile GPUs

**Publication:**

MICRO’18

**Problem to solve:**

With the continuously improved performance of mobile GPUs, local processing has
become a promising solution to the large data transmission and privacy issues
induced by the cloud-centric computations of IPAs. However, LSTMs exhibit quite
inefficient memory access pattern when executed on mobile GPUs due to the
redundant data movements and limited off-chip bandwidth.

**Major contribution:**

1.  INTER-CELL LEVEL OPTIMIZATIONS

    1.  The Irrelevance Between Two LSTM Cells

>   In LSTM, the activation functions are sigmoid and tanh. This paper finds
>   that when the input is in the range of [−2, 2], its output is nearly linear
>   to the input, they refer it as sensitive area. On the other hand, its output
>   is insensitive to the input within the range of [−∞,−2] and [2,+∞], they
>   refer it as insensitive area.

>   According to the computing equation of LSTM, this paper finds that when the
>   input is in the insensitive area, the previous cell’s output ht−1 can be
>   considered as irrelevant to the current cell’s output ft, it, ct, and ot,
>   thus, having no impact to the current cell’s computation. In other words,
>   there is no context link between these two cells.

1.  LSTM Layer Division

>   Based on the above observation that the context links between every two
>   cells are not uniform throughout the LSTM layer, they propose the LSTM layer
>   division scheme which breaks the context link between cells with no or quite
>   weak link so that a LSTM layer is divided into multiple independent

>   sub-layers.

1.  LSTM Layer Reorganization

>   Tissue Formation: Given the independent LSTM sub-layers, they parallelize
>   them via fusing cells from the sub-layers into tissues. One cell will be
>   selected per sub-layer, and the selected cells together form a tissue.
>   Ideally, when there are more sub-layers and more cells are fused into a
>   tissue, there will be fewer tissues in the layer and thus, fewer re-loads
>   for the weight matrices and performance are improved as well. However, they
>   observe that keeping increasing the tissue size would even hurt the
>   performance. Further increasing the tissue size would cause the kernel
>   re-configuration at the compilation time to ensure that the on-chip
>   bandwidth utilization is below 100%.

>   Tissue Alignment: Since the tissue formation mechanism simply combines
>   multiple cells into tissues but ignores the MTS, it may generate both fat
>   and thin tissues. Fat tissues have more cells than MTS leading to the
>   over-utilized share-memory bandwidth, while thin tissues have quite few
>   cells and are unable to effectively reuse the weight matrix. To maximize the
>   performance, they explore the tissue alignment mechanism to well balance the
>   tissue size by moving cells from the fat tissues to thin tissues, e.g.
>   moving cell7 and 8 from Tissue0 and Tissue1 to Tissue1 and Tissue2,
>   respectively.

1.  INTRA-CELL LEVEL OPTIMIZATIONS

>   Besides the redundant data movements across cells, the off-chip memory
>   bandwidth is the other major performance limitation for each LSTM cell.
>   Since weight matrix Uf,i,c,o is the largest input data for one cell, it is
>   important to shrink it, hence addressing the bottleneck inside the LSTM
>   cell.

>   Noticing that weights in LSTM are processed in the row order, and
>   especially, the elements from different rows are totally irrelevant. They
>   leverage this unique feature to propose the row-level weight compression
>   technique, called dynamic row skip, which compacts weights in the matrix at
>   the row level without affecting the output accuracy. To be specific, they
>   dynamically skip those irrelevant rows in the weight matrices Uf , Ui, Uc
>   whose computations have trivial contribution to the cell output vector ht.
>   By doing this, the skipped rows will not be loaded and their computations
>   are ignored as well, leading to both performance and energy optimizations.

**Lessons learnt:**

This paper aims to explore the memory friendly LSTM on mobile GPUs by
hierarchically reducing the off-chip memory accesses. The observation of
sensitive and insensitive area is quite interesting, and guides them to explore
sub-layer division.
