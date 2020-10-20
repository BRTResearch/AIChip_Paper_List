**Paper title:**

ShapeShifter: Enabling Fine-Grain Data Width Adaptation in Deep Learning

**Publication:**

MICRO’19

**Problem to solve:**

1.  Quantization to the shortest data width possible is especially appealing for
    Deep Learning workloads for two reasons: First, most of their energy
    expenditure is due to data transfers. Using a short data type reduces the
    volume of this data. Second, since the data is input to numerous
    multiply-accumulate (MAC) operations which exhibit great data parallelism,
    the shorter the data type, the more functional units we can deploy for a
    given on-chip area and the higher performance and energy efficiency.

2.  We observe that data widths can be trimmed further since: 1) by design, the
    expected per-layer distribution of values in deep learning models. For
    weights or activations, most will be near zero and few will be of higher
    magnitude, and 2) which values will assume a high magnitude will vary with
    the input.

3.  However, the data width used at any given point of time needs to accommodate
    only 1) the activation values for the specific input at hand, and further 2)
    the activation and weight values that are being processed or transferred
    concurrently.

**Major contribution:**

1.  The key idea proposed in this work is to use per group data width
    adaptation, where a group is a set of values that are either calculated upon
    or transferred from/to memory together. We propose to select the data width
    dynamically for activations and statically for weights.

2.  Our first contribution is to show that adjusting the data width per group
    dynamically for activations and statically for weights yields much shorter
    effective data widths than even per layer width selection. As our second
    contribution, we bring attention to a property of popular quantization
    methods is that while they successfully “squeeze” broader value ranges to
    fit within a target data width, they also “expand” shorter data ranges into
    the target data width..

3.  Our first novel hardware technique is a low cost lossless memory compression
    method that is plug-in compatible with most Deep Learning hardware. Our
    second novel hardware technique adapts the width of activations and weights
    at runtime so that execution time is proportionally reduced per group of
    concurrently processed values.

**Lessons learnt:**

In this paper, the existing problems of traditional quantization are analyzed,
and a method of hardware and software co-quantization is proposed, which can
match a variety of hardware and have experiments on multiple models. Per group
precision adaptation opens up several directions for future work including how
to combine with other accelerator engines.
