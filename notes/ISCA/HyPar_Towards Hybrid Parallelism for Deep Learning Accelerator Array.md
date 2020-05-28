**Paper title:**

HyPar: Towards Hybrid Parallelism for Deep Learning Accelerator Array

**Publication:**

HPCA’19

**Problems to Solve:**

Hardware acceleration of DNNs is intensively studied to achieve high performance
and energy efficiency. But most accelerators focus on acceleration for DNN
inference, while training is performed by high-performance computer systems with
high-end CPUs/GPUs, which are not performance and energy efficient.

In order to provide high throughput and energy efficient acceleration for
training deep and large models, using multiple accelerators to enhance
coarse-grain parallelism is a straightforward but effective method. The problem
is how to organize computation and dataflow among accelerators so that best
performance and energy efficiency can be achieved.

**Major Contributions:**

The problem is challenging due to the complex interactions between the type of
parallelism and different layers. Typically, there are two types of parallelism
for partitioning training of each layer into multiple accelerators, data
parallelism and model parallelism. Which parallelism manner to choose for each
layer can be phrased as a complex optimization problem because of the
complicated intra-/inter-layer communications among accelerators. This paper
systematically solves this problem step by step and major contributions can be
summarized as follows:

-   This paper proposes a communication model to explain where the communication
    comes from in partitioned tensors (of feature maps and kernels), and
    determines the amount of communication. The communication model analyzes
    intra-layer and inter-layer communication for both data parallelism and
    model parallelism.

-   This paper proposes a hierarchical layer-wise dynamic programming method to
    search for the partition for each layer. The optimization target is to
    search a partition that minimizes the total communication during training a
    complete deep neural network. Rather than O(2N) brute force search, the
    proposed method is heuristic and practical: the time complexity for the
    partition search is linear, i.e. O(N) for a neural network with N weighted
    layers.

-   To expand to partition for an array of accelerators, this paper proposes a
    hierarchical approach and applies this method in an HMC-based DNN training
    architecture with an array of sixteen accelerators organized in four
    hierarchical levels and minimize the data movement.

-   This paper evaluates on ten DNN models from classic Lenet to large-size
    model VGGs, and the number of weighted layers of these models ranges from
    four to nineteen. Results show hybrid parallelism can be better than either
    the default Data Parallelism or Model Parallelism in DNN training with an
    array of accelerators, and more specifically, a performance gain of 3.39×
    and an energy efficiency gain of 1.51× compared to Data Parallelism on
    average.
