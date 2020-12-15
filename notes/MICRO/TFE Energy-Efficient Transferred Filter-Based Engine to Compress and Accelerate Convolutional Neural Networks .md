**Paper Title:**

TFE: Energy-Efficient Transferred Filter-Based Engine to Compress and Accelerate
Convolutional Neural Networks

**Publication:**

MICRO’2020

**Problem to solve:**

Deep CNNs have achieved great success in many fields. However, these works
largely rely on millions of parameters and computations to achieve high
accuracy. Many studies have made efforts in alleviating these problems, one of
which is transferred filter-based algorithms. But the problem is that
transferred filter-based algorithms result in massive redundant repetitive
computations, which causes significant energy consumption. In this work, a
transferred filter-based engine (TFE) is proposed to compress the CNN model size
and accelerate the compressed CNN models in a hardware-friendly manner without
large overhead.

**Main contribution:**

1.  The TFE is the first systematic solution that exploits transferred
    filter-based algorithms to significantly compress and accelerate CNN models.

2.  Two hardware-friendly techniques, PPSR and ERRR, are proposed in the TFE to
    eliminate hidden repetitive computations inside and among transferred filter
    rows. Therefore, the merging of the two techniques remove all duplicate
    computations in transferred filters, significantly accelerating CNN
    implementations.

3.  An efficient TFE hardware architecture is developed to use SAFM to
    efficiently support various filters. SAFM adopts the PE sub-array as the
    basic computational unit where input data can be efficiently broadcast,
    which can substantially decrease the area overhead and power consumption of
    the CNN implementation.
