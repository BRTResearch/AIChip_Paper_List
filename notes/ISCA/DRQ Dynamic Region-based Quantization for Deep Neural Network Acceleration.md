**Paper title:**

DRQ: Dynamic Region-based Quantization for Deep Neural Network Acceleration

**Publication:**

ISCA’20

**Problem to solve:**

Quantification is an effective method for deep neural networks to accelerate
inference. However, traditional quantization techniques are either applied to
the network level or layer by layer, and cannot be further accelerated by
fine-grained quantization, or only applied to the kernel weights, regardless of
the dynamic changes of the feature maps, which may lead to a decrease in the
accuracy of the neural network.

**Major contribution:**

To tackle the above problems, the paper proposes a novel dynamic region-based
quantization, termed as DRQ, to capture the feature characteristic in the input
feature map for quantization. The contributions are as follows:

1.  Based on experiments, the authors find that some of the input values are
    highly correlated with the NN accuracy, termed as the sensitive values. In
    addition, these sensitive values tend to aggregate in a region. The
    observation implies that applying high fidelity quantization on the
    sensitive regions will reserve the NN accuracy, while applying low-fidelity
    quantization on the insensitive regions can boost the performance.

2.  The paper proposes an algorithm to identify the sensitive regions at run
    time. The algorithm can be instantiated as a just-in-time predictor, which
    can be neatly embedded after each convolution layer to predict the
    sensitivity of the input values for the next layer.

3.  This paper proposes an accelerator design to support the dynamic
    region-based quantization. It applies a simple but fine-grained control
    scheme that can perform high-precision computation for the sensitive regions
    and low-precision computation for the insensitive regions.

**Lessons learnt:**

Conventional schemes only support network- or layer-wise quantization. But DRQ
can support sub-layer and even sub-feature-map quantization, which can provide
more freedom for fine-grained tuning. Algorithms and architectures are often
combined to achieve greater performance improvements.
