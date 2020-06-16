**Paper title:**

A3: Accelerating Attention Mechanisms in Neural Networks with Approximation

**Publication:**

HPCA’20

**Problem to solve:**

Attention based NN spends a notable amount of time in attention par, and most NN
accelerators are not considering this part. So, this paper tries to propose an
accelerator for attention based NN.

**Major contribution:**

1.  Quantify the attention mechanism bottlenecks in NN models.

2.  An approximation scheme which can avoid an exhaustive search to reach a
    better time performance.

3.  A specialized hardware pipeline for an attention mechanism exploiting
    parallelism and datapath specialization to significantly improve the
    performance and energy efficiency of the attention mechanism.

**Lessons learnt:**

Attention based NN is relatively new and very popular in NLP area.
