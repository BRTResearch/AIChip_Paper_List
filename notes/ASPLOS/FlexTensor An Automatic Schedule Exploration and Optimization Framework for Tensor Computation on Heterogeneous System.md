**Paper title:**

FlexTensor: An Automatic Schedule Exploration and Optimization Framework for
Tensor Computation on Heterogeneous System

**Publication:**

ASPLOS’20

**Problem to solve:**

1. High-performance tensor computation libraries suitable for specific platform
take months or even years to develop.

2. Specific hardware architecture have many optimization schedules and
parameters to decide, which may cause a sub-optimal implementation.

3. Manual implementation hardly portable to other platforms.

**Major contribution:**

They develop a framework based on TVM called FlexTensor to automatically
generate schedule for CPU, GPU and FPGA. Given a mathematical description of
tensor computation, FlexTensor will automatically decide how to map the tensor
algorithms onto different low-level platform. FlexTensor is composed of two
parts: the front-end and the back-end.

The front end analyzes the static information of tensor computation and generate
schedule space. The static information includes two categories: statistical
information and structural information correspond to the characteristics of
graph nodes and edges. The schedule space enumerates different combinations of
schedule primitives. Same type of primitives is encoded using a vector.

The back-end is used for find the schedule to get highest performance. They use
a heuristic method based on simulated annealing. This method is aim at finding a
vector having the highest performance value. Then, Q-learning are performed to
predict the best direction of the vector.

In the experiments, they test 12 different kinds of tensor computations with
totally hundreds of test cases and FlexTensor achieves average 1.83x performance
speedup on NVIDIA V100 GPU compared to cuDNN; 1.72x performance speedup on Intel
Xeon CPU compared to MKL-DNN for 2D convolution; 1.5x performance speedup on
Xilinx VU9P FPGA compared to OpenCL baselines; 2.21x speedup on NVIDIA V100 GPU
compared to the state-of-the-art.
