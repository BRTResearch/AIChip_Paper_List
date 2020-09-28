**Paper title:**

FA3C: FPGA-Accelerated Deep Reinforcement Learning

**Publication:**

ASPLOS’19

**Problem to solve:**

1. Deep RL training is based on the datasets generated while the training itself
is happening. Because of this, performance improvement by exploiting
massively-parallel computing resources in a GPU for a large number of training
data samples may not be possible during Deep RL training.

2. The Asynchronous Advantage Actor-Critic (A3C) algorithm and its variants are
considered as state-of-the- art Deep RL algorithms. A3C training is performed
with small computation batches resulting in low GPU utilization.

**Major contribution:**

In this paper, they propose an FPGA-based A3C Deep RL platform called FA3C. It
has higher energy efficiency than GPU-based platform, low execution latency even
with frequent kernel launches, and customizable memory subsystems.

A3C algorithm is executed on heterogeneous system consist of FA3C and CPU. Each
agent in CPU memory is sent to the individual thread in FA3C according to the
PCI-E Express. The data sent to the FA3C comprise of screen scene input and
inference request. The output of FA3C is the feature map of the most outer layer
of DNN in A3C and next action. The point of the action is computed in the
environment simulator of CPU. In the training stage, the CPU send objective
function and gradient to FA3C.

The DRAM of FA3C stores the private argument of agent consist of DNN argument
local θ and feature map that are used for inference stage. Gradient and RMS g
are arguments used in training stage. All agents share global θ which update in
training stage. They use RMSProp optimizer in training stage.

FA3C has many CU pairs for inference and training. Each CU execution one stage
in DNN computation. A CU consists of on-chip memory and many PEs which can
handle the computation of forward propagation, backward propagation and
gradient. On-chip memory comprise of Parameter buffer, Feature-map buffer and
Gradient buffer with corresponding line buffer to store the different types of
data. Parameter buffer etc can efficient utilize DRAM interface and buffer data
from DRAM. Line buffers prefetch different position in Parameter buffer etc and
preprocess data by shifting, merging and cropping. Line buffer stores the source
data of PEs. There are many MUXs between on-chip memory and PEs to control data
transmission because PEs may get data from different types of buffers. Also, PEs
send data to on-chip memory by DEMUX.

RMSProp Module in CU is used for gradient computation. As the bandwidth of DRAM
interface is 16 words, RMSProp consists of 4 RUs that read 2 words and produce 2
words in each cycle. RU can handle multiplication, addition and division to
update RMS g and global θ.

As for different computation stage, parameter layout in the buffer is different.
Parameters are divided into 16×16-word tile to satisfy the bandwidth of DRAM
interface. When computing forward propagation, a PE need I×K2(I stand for the
number of channel of input feature map, K is the size of filter) cycles to
output a feature map. When computing backward propagation, the filter is
transported by Transport Load Unit. If the backward propagation layout is same
as the forward, all PEs calculate input gradients of a single input channel
only. In this case, the computation throughput can be increased by calculating
multiple input gradients of the same input channel simultaneously. However, a
large amount of output gradients have to be accessed simultaneously because
different input gradients in the same input channel are associated with
different regions of the output feature maps.

FA3C achieves 27.9% better performance than that of a state-of-the-art GPU-based
implementation. Moreover, the energy efficiency of FA3C is 1.62× better than
that of the GPU-based implementation.

**Lessons learnt:**

1. I have learnt the basic knowledge of reinforcement learning and the
calculation process of A3C algorithm.

2. The core idea of ​​the paper is that when the A3C algorithm is implemented by
GPU, the GPU utilization rate in the inference and training stage is low.
FPGA-based implementation is more suitable for specific algorithm.

3. Different layout in the buffer between inference stage and training stage can
effectively utilize PE resources.
