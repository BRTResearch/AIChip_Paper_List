**Paper title:**

PUMA: A Programmable Ultra-efficient Memristor-based Accelerator for Machine
Learning Inference

**Publication:**

ASPLOS’19

**Problem to solve:**

Previous designs lack several important features for supporting general ML
workloads.

First, each design supports one or two types of neural networks, where layers
are encoded as state machines. This approach is not scalable to a larger variety
of workloads due to increased decoding overhead and complexity.

Second, existing accelerators lack the types of operations needed by general ML
workloads. For example, Long Short-Term Memory (LSTM) workloads require multiple
vector linear and transcendental functions which cannot be executed on crossbars
efciently and are not supported by existing designs.

Third, existing designs do not provide ﬂexible data movement and control
operations to capture the variety of access and reuse patterns in diﬀerent
workloads. This data movement can amount to a signifcant portion of the total
energy consumption which calls for ﬂexible operations to optimize the data
movement.

**Major contribution:**

1.  Propose PUMA’s microarchitecture techniques exposed through a specialized
    Instruction Set Architecture (ISA) retain the efciency of in-memory
    computing and analog circuitry, without compromising programmability.\\

2.  Present the PUMA compiler which translates high-level code to PUMA ISA. The
    compiler partitions the computational graph and optimizes instruction
    scheduling and register allocation to generate code for large and complex
    workloads to run on thousands of spatial cores.

3.  Develope a detailed architecture simulator that incorporates the
    functionality, timing, and power models of PUMA’s components to evaluate
    performance and energy consumption.

A PUMA accelerator running at 1 GHz can reach area and power efciency of 577
GOPS/s/mm2 and 837 GOPS/s/W, respectively. Our evaluation of diverse ML
applications from image recognition, machine translation, and language modelling
(5M-800M synapses) shows that PUMA achieves up to 2,446× energy and 66× latency
improvement for inference compared to state-of-the-art GPUs. Compared to an
application-specifc memristor-based accelerator, PUMA incurs small energy
overheads at similar inference latency and added programmability.

**Lessons learnt:**

1.  The DNN operator based RRAM accelerator is more comprehensive. The
    instruction set architecture (ISA), simulator, etc., are all designed by
    themself, which is not found in the RRAM accelerator. Previous accelerators
    only focus on architecture.

2.  PUMA is a spatial architecture organized in three-tiers: cores, tiles, and
    nodes. Cores consist of analog crossbars, functional units, and an
    instruction execution pipeline. Tiles consist of multiple cores connected
    via a shared memory. Nodes consist of multiple tiles connected via an
    on-chip network. Subsequently, nodes can be connected together via a
    chipto-chip interconnect for large-scale execution
