**Paper title:**

Neural Cache: Bit-Serial In-Cache Acceleration of Deep Neural Networks

**Publication:**

ISCA’18

**Problem to solve:**

The cost of data movement had caused memory wall problem for a long time. Near
data computing is one of the solution. But the authors thought computation in
DRAM is far from processor. So they proposed a novel cache architecture to
support DNN’s computation.

**Major contribution:**

1.  Architecture which is a compute SRAM array design that is capable of
    performing additions and multiplications. A critical challenge for enabling
    complex operations in cache is facilitating interaction between bit lines.
    They propose a novel bit-serial implementation with transposed data layout
    to address the above challenge.

2.  Architecture *Neural Cache* which harnesses the full potential of in-cache
    compute capabilities to accelerate DNN inferences. The main method is
    exposing the parallelism in DNN computation to the underlying cache
    geometry.

The proposed architecture can improve inference latency by 18.3× over
state-of-art multi-core CPU (Xeon E5), 7.7× over server class GPU (Titan Xp),
for Inception v3 model. Neural Cache improves inference throughput by 12.4× over
CPU (2.2× over GPU), while reducing power consumption by 50% over CPU (53% over
GPU).

**Lessons learnt:**

Near data computing is not a new idea nowadays. But computable cache with
support for DNN is interesting as neural network still needs new kinds of
accelerators. Bit-serial computable cache provided high parallelism for DNN’s
computation. An example layout for a single array is shown as below.
