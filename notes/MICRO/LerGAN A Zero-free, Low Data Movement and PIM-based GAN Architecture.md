**Paper Title:**

LerGAN: A Zero-free, Low Data Movement and PIM-based GAN Architecture

**Publication:**

MICRO’2018

**Problem to solve:**

There are two challenges of PIM-based GAN accelerator:

1.  Redundant zero-related operations. Zero-insertion during training phase adds
    a heavy burden on storage.

2.  Inefficient I/O connection. Complex dataflow patterns between the two models
    result in I/O traffic which become the system bottleneck.

And training a GAN imposes three more challenges:

>   1) Intensive communication caused by complex train phases of GAN

>   2) Much more ineffectual computations caused by special convolutions

>   3) more frequent off-chip memory accesses for exchanging inter-mediate data
>   between the generator and the discriminator.

**Major contribution:**

1.  Elaborate three steps of zero-inserting that enable transposed convolution
    operations in GAN and further analyze the amount of zeros in GAN training.
    To address problems caused by massive zeros in ReRAM-based PIM, propose
    Zero-Free Data Reshaping (ZFDR) to remove zero-related operations. ZFDR is
    flexible to support different paddings, strides and kernel sizes, capable of
    handling both existing GANs and future GANs with larger stride.

2.  Present the dataflows of training GAN in detail and propose a novel
    reconfigurable 3D-connected PIM to handle the complicated dataflows. 3D
    connection supports efficient data transferring of both propagation and
    updating.

3.  Propose LerGAN based on ZFDR and 3D-connected PIM to address the challenges
    of training GAN. Enable programmers to use heterogeneous levels of
    acceleration according to demands.
