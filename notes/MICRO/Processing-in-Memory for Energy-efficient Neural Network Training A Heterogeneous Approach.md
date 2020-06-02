**Paper title:**

Processing-in-Memory for Energy-efficient Neural Network Training: A
Heterogeneous Approach

**Publication**:

MICRO’18

**Problem to solve:**

Heterogeneous PIM architecture introduces multiple challenges in the programming
method and runtime system:

1.  Programming PIMs to accelerate NN training is nontrivial. In order to
    improve productivity and ease-of-adoption of PIM-based NN training
    accelerators, we need to develop a programming method that maximizes code
    reuse without asking the programmer to repeatedly program on different PIMs.

2.  Combining fixed-function logics and programmable cores in PIM further
    complicates the software design. Fixed function and programmable PIMs employ
    vastly different programming models: Fixed-function PIMs employ ISA-level
    instructions accessed via assembly-level intrinsics or via library calls;
    Programmable PIMs employ standard programming paradigms, such as threading
    packages or GPGPU programming interfaces. Most previous PIM designs adopt
    homogeneous PIM architectures– with either fixed-function or programmable
    PIMs – which allows a simplified software interface design. But with
    heterogeneous PIM, it is critical to design a unified programming model that
    can accommodate both PIM components.

3.  The scale of operations in NN training can lead to unbalanced hardware
    utilization. Ideally, we want to achieve high utilization of PIMs. However,
    it can be difficult to achieve. So ,in such a heterogeneous system by pure
    hardware scheduling, because of the complexity of tracking operation
    dependency and synchronization. Furthermore, NN training typically adopts a
    large amount (e.g., tens of thousands) of iterative steps and hundreds of
    operations per step. Operation dependency across the massive amount of steps
    and operations can impose synchronization overhead and decrease hardware
    utilization, when operations are running on multiple computing devices.

**Major contribution:**

Design a PIM-based NN training acceleration system that can efficiently
accelerate unmodified training models written on widely-used machine learning
frameworks. The design consists of three components: 1) adopt a heterogeneous
PIM architecture, which integrates both fixed-function logics and programmable
cores in 3D diestacked main memory. 2) extend the OpenCL programming model to
address the programming challenges. The programming model maps the host CPU and
heterogeneous PIMs onto OpenCL’s platform model and extends OpenCL’s execution
and memory models for efficient runtime scheduling. 3) propose a runtime system,
which maximizes PIM hardware utilization and NN-operation-level parallelism.

**Lessons learnt:**

Heterogeneous PIM accelerator and its hardware/software co-design is hot
research direction of DNN accelerator, mainly to solve the problem of high
overhead of data transfer.There are many innovative points in this paper.
Processing unit and storage unit in the large architecture design, the
architecture design of combining CPU and PIM, and the programmable PIM are all
very important points.
