**Paper title:**

Bridging the Gap Between Neural Networks and Neuromorphic Hardware with A Neural
Network Compiler

**Publication:**

ASPLOS '19

**Problem to solve:**

Designing custom chips for NN applications with the Very-Large-Scale-Integration
(VLSI) technologies has been investigated as a power-efficient and
high-performance alternative to general-purpose computing platforms such as CPU
and GPU. However, programming these chips is difficult because of some
hardware-specific constraints: 1. Due to the utilization of hardware resources
for digital circuits or the capability of analog computing for some
memristor-based designs, the precision of input and output signals of neurons is
usually limited, 2. the precision of NN parameters, such as synaptic weights. 3.
The present fabrication technology limits the fan-in and fan-out of one neuron,
which constrains the computation scale. 4. The diversity of nonlinear functions
or neuron models supported by the hardware is also limited. For example, for
TrueNorth chips, the maximum matrix that one synaptic core can handle is 256 ×
256, and it supports only a simplified leaky–integrate-and-fire (LIF) neuron
model.

However, the existing methods addressing the aforementioned challenges highly
depends on the redundancy in NN models. Different NN models may have different
minimum requirement (precision, connectivity, etc.) on hardware. Thus,
transforming procedure is not a general method, especially for NN models with
less redundancy and hardware with severe constraints.

**Major contribution:**

An NN transformation workflow is presented to convert a trained NN, expressed as
a CG, into an equivalent representation of HW/SW interface to support different
types of NNs. The SW/HW interface is easy to be adapted to different NN
hardware.

Such a toolchain is implemented to support two different hardware designs’
constraints, a real CMOS neuromorphic chip for ANN&SNN, TianJi, and a PIM design
built upon metal-oxide resistive random access memory (ReRAM) for ANN, PRIME.

Complete quite a few evaluations of various metrics. The extra error caused by
this process is very limited and time overhead is much less (compared to the
whole training process of the original NN). In addition, its sensitivity to
different configurations and transformation strategies has been explored
comprehensively.
