**Paper title:**

eCNN: A Block-Based and Highly-Parallel CNN Accelerator for Edge Inference

**Publication:**

MICRO’19

**Problem to solve:**

Convolutional neural networks (CNNs) have recently demonstrated superior quality
for computational imaging applications. Therefore, they have great potential to
revolutionize the image pipelines on cameras and displays. However, it is
difficult for conventional CNN accelerators to support ultra-high-resolution
videos at the edge due to their considerable DRAM bandwidth and power
consumption. Therefore, finding a further memory- and computation-efficient
microarchitecture is crucial to speed up this coming revolution.

In this paper, they apply a block-based inference flow which can eliminate all
the DRAM bandwidth for feature maps and accordingly propose a hardware oriented
network model, to optimize image quality based on hardware constraints.

**Major contribution:**

-   This paper proposes a block-based flow to enable high-resolution inference
    with low DRAM bandwidth and also analyze its computation and bandwidth
    overheads

-   This paper proposes a hardware-aware ERNet to optimize image quality based
    on hardware constraints and also builds training procedures for model
    optimization and dynamic fixed-point precision.

-   This paper devises the SIMD instruction set, FBISA, to support the truncated
    pyramid inference for fully convolutional networks. Fig. 4 shows the
    instruction format. An opcode can specify a convolution task with specific
    attributes, e.g, inference type and block size. The smallest computing task
    in FBISA is called a 32ch-to-32ch CONV3×3 filter on one feature block. The
    weights are compressed to increase the supported model size, and we adopt
    the DC Huffman coding in JPEG.

-   This paper designs an embedded processor, eCNN, to support the block based
    algorithm.

**Lessons learnt:**

This paper proposes a novel NN inference flow---block based execution flow.
However, due to the receptive field, this paper can only be applied to shallow
networks, or a brand new model.
