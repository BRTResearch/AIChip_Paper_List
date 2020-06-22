**Paper title:**

NEUTRAMS: Neural Network Transformation and Co-design under Neuromorphic
Hardware Constraints

**Publication:**

MICRO’16

**Problem to solve:**

Another computing paradigm, neuromorphic computing, is emerging as a hot scheme
with associated design and fabrication of neuromorphic chips. To address the
difficult of programming for neuromorphic computing, this paper proposed a
systematic methodology with a set of tools. The tool is necessary to be designed
to bridge the gap between applications and neuromorphic hardware.

**Major contribution:**

1.  This paper proposed a hardware-independent representation layer of neural
    network to describe high-level NN models to satisfy the hardware constraints
    of a neuromorphic chip.

2.  This paper designed a training-based transformation algorithm to transform
    an existing NN described by the above representation into its counterpart
    under the target hardware’s constraints.

3.  This paper implemented a configurable, clock-driven simulator to achieve
    performance and power simulation on the microarchitecture level, supporting
    different types of neuromorphic cores and memory technologies.

4.  This paper proposed an optimized strategy to map the trained NNs onto
    neuromorphic hardware, using graph partition algorithm to put densely
    communicating neurons together.

5.  This paper implemented such a toolchain for a real CMOS neuromorphic
    processor and for a processing-in-memory architecture design for ANNs,
    guiding the optimization of hardware design.

**Lessons learnt:**

1.  Learning hint from this paper, employing a neuromorphic technique to form
    the general system for diverse NNs, such as SNNs, CNNs, RNNs and MLPs, may
    come a high-level value. As such, designing a novel architecture for a large
    chip domain, break through the fundamental architecture such von Neumann
    architecture may bring an insight into the designing space.

2.  From an abstract idea to a visual general implements, a set of toolchains or
    evaluators is essential process. Of these, toolchains can help achieve the
    mapping among preliminary idea and hardware/software. Subsequently, the
    error-rates and hardware constraints and consumptions may be the target,
    worthy of achieving.
