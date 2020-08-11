**Paper title:**

SC-DCNN: Highly-Scalable Deep Convolutional Neural Network using Stochastic
Computing

**Publication:**

ASPLOS’17

**Problem to solve:**

1.  Despite the performance and power (energy) efficiency achieved, a large
    margin of improvement still exists due to the inherent inefficiency in
    implementing DCNNs using conventional computing methods or using
    general-purpose computing devices。

2.  In SC, probability number is represented using a bit-stream, therefore, the
    key arithmetic operations such as multiplications and additions can be
    implemented as simple as AND gates and multiplexers (MUX), respectively. Due
    to these features, SC has the potential to implement DCNNs with
    significantly reduced hardware resources and high power (energy) efficiency.

**Major contribution:**

1.  Applying SC to DCNNs. We are the first (to the best of our knowledge) to
    apply SC to DCNNs. This approach is motivated by 1) the potential of SC as a
    computing paradigm to provide low hardware footprint with high energy
    efficiency and scalability; and 2) the need to implement DCNNs in the
    embedded and mobile IoT devices.

2.  Basic function blocks and hardware-oriented max pooling. We propose the
    design of function blocks that perform the basic operations in DCNN.
    Specifically, we present a novel hardware-oriented max pooling design for
    efficiently implementing (approximate) max pooling in SC domain. The pros
    and cons of different types of function blocks are also thoroughly
    investigated。

3.  Joint optimizations for feature extraction blocks. We propose four optimized
    designs of feature extraction blocks which are in charge of extracting
    features from input feature maps. The function blocks inside the feature
    extraction block are jointly optimized through both analysis and experiments
    with respect to input bit-stream length, function block structure, and
    function block compatibilities.

4.  Weight storage schemes. The area and power (energy) consumption of weight
    storage are reduced by comprehensive techniques, including efficient
    filter-aware SRAM sharing, effective weight storage methods, and layer-wise
    weight storage optimizations.

5.  Overall SC-DCNN optimization. We conduct holistic optimizations of the
    overall SC-DCNN architecture with carefully selected feature extraction
    blocks and layerwise feature extraction block configurations, to minimize
    area and power (energy) consumption while maintaining the high network
    accuracy. The optimization procedure leverages the crucial observation that
    hardware inaccuracies in different layers in DCNN have different effects on
    the overall accuracy. Therefore, different designs may be exploited to
    minimize area and power (energy) consumptions。

**Lessons learnt:**

1.  This is the first Stochastic Computing of the article in the CNN
    accelerator, which is of great significance to the exploration of
    convolution, pooling, activation function and weight storage schem.

2.  The disadvantage is that the application of stochastic calculation in Lenet5
    is analyzed. Although this includes the basic components of CNN, the data
    flow and calculation process are relatively simple.
