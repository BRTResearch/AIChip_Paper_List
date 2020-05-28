**Paper title:**

Energy-efficient neural network accelerator based on outlier-aware low-precision
computation

**Publication:**

ISCA’18

**Problem to solve:**

Owning to the presence of large values, which we call outliers, conventional
methods of quantization fail to achieve significantly low precision, e.g., four
bits for very deep neural networks, such as ResNet-101. Based on statistical
analysis on weight values, a novel quantization method called *outlier-aware
quantization*, which divides the distribution of data (mainly weights) into two
regions, of low and high precision to solve the problem.

**Major contribution:**

1.  This paper proposes an accelerator called OLAccel that implements 4-bit
    computations on very deep CNNs which differently handling outlier
    activations and weights to improve computational efficiency.

2.  OLAccel could perform sparse high-percision computation for outlier
    activations in parallel with dense low-precision computation for a majority
    of activations, which could reduce latency. This is achieved through
    equipping SIMD lanes with an outlier MAC unit.

3.  This paper designs OLAccel in Verilog and compare it with prevalent
    accelerators, Eyeriss and ZeNA at reduced precision.

**Lessons learnt:**

This paper has realized a new CNN accelerator to support a novel quantization
method and could greatly save energy consumption. It proposes a quantization
architecture that could adapt to weigh value distributions, but the accuracy
loss sometimes can not be neglected.

The results show that the OLAccel can reduce by 43.5% (27.0%), 56.7% (36.3%),
and 62.2% (49.5%) energy consumption for AlexNet, VGG-16, and ResNet-18,
respectively, compared with a 16-bit (8-bit) state-of-the-art zero-aware
accelerator. The energy gain mostly comes from the memory components, the DRAM,
and on-chip memory due to reduced precision.
