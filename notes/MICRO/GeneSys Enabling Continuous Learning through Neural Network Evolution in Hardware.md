**Paper title:**

GeneSys: Enabling Continuous Learning through Neural Network Evolution in
Hardware

**Publication:**

MICRO’18

**Problem to solve:**

1. Supervised learning may break while occurring unavailability of structure
labeled data, unknown Network topology, dynamically changing problem and
limitation of computation resource for training.

2. Reinforcement learning and evolutionary algorithm can handle changing
environment but backpropagation consume large computation resource.

3. Deploying the RL and EA on robots or drones demands extremely high
energy-efficiency.

**Major contribution:**

They design a SOC called GENESYS to accelerate an EA-based learning system.
GENESYS comprises of a learning engine called EvE , an inference engine called
ADAM, a CPU for controlling dataflow and a SRAM-based buffer that storing data.

CPU pre-conduct the data from the buffer. As NNs are initialized to
full-connection but edge is zero, children NNs generated from the type of parent
NNs are very sparse. CPU translate sparse NN into dense matrix multiplication in
inference. In EA algorithm, only high fit parent can send their gene to
children. CPU send the proper data to EvE to generate new NNs.

ADMA consists of a systolic array of MAC units to perform inference. ADMA
receive environment state and NN topology with weight from CPU. AMDA output
agent action to environment.

EvE is used to generate new NNs. It consists of a collection of PEs, designed
for power efficient implementation of crossover and mutation operations. PEs
handle four types of computation: crossover, perturbation mutation, delete gene
mutation and add gene mutation. Pseudo Random Number Generator feed random
numbers to PEs as computation mentioned above need random numbers. The Gene
Split Block align parent gene between Buffer and EvE PEs. The Gene Merge block
merge genes from PEs into genome(NNs).

SRAM-based Buffer is used to store the NNs with fitness value.

They build a GENESYS SoC in 15nm, and evaluate it against optimized NE
implementations over latest embedded and desktop CPUs and GPUs. We observe 2-5
orders of magnitude improvement in runtime and energy-efficiency
