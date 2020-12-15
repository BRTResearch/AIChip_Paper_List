**Paper title:**

Towards Efficient Microarchitectural Design for Accelerating Unsupervised
GAN-Based Deep Learning

**Publication:**

ISCA’2018

**Problem to solve:**

1.  IoT nodes are normally sensitive to power consumption, where the
    power-hungry GPU is not applicable. Therefore, it is imperative to propose a
    power efficient GAN accelerator deployed on IoT nodes for on-line
    unsupervised learning.

2.  The unsupervised learning represented by GAN training involves more complex
    computations, including strided convolutions, transposed convolutions, and
    four-dimension convolutions. Although these operations could still utilize
    traditional CNN accelerators, the differences in the computing pattern, such
    as zero-inserting, result in low efficiency of existing CNN accelerators.
    Moreover, GAN training has more computing phases since it includes two
    networks' (Generator and Discriminator) updates. Therefore, the distinct
    features of GAN challenge the current deep learning accelerator designs and
    demand customized microarchitectural optimizations to efficiently implement
    GAN.

3.  We demonstrate the following challenges in GAN accelerator design by
    thoroughly analyzing the procedure of GAN training. First, the
    synchronization operation (for loss calculation) in GAN training not only
    demands large memory to store the intermediate data but also restricts the
    parallel optimization. Second, the abundant and variable computing phases
    and the non-traditional convolutional operations in these phases further
    complicate the accelerator design.

**Major contribution:**

1.  We take the first step to help computer architecture community to understand
    the inefficiencies of current accelerators to support unsupervised training.

2.  This paper is the first work that presents the holistic solution for
    accelerating the unsupervised deep learning.

3.  The proposed design features two novel micro architectures (ZFOST and ZFWST)
    and high-efficiency dataflows tailored for the non-traditional convolutions:
    S-CONV, T-CONV and W-CONV. It is worth pointing out that these
    microarchitectural optimizations can also be widely used in traditional CNN
    training procedure.
