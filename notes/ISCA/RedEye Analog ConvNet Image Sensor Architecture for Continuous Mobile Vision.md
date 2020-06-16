**Paper title:**

RedEye: Analog ConvNet Image Sensor Architecture for Continuous Mobile Vision

**Publication:**

ISCA’2016

**Problem to solve:**

Continuous mobile vision has recently attracted attention, but it faces a
daunting barrier: energy efficiency. This is largely due to the energy burden of
analog readout circuit, data traffic, and intensive computation. The analog
readout bottleneck need to be solved urgently.

**Major contribution:**

1.  The paper presents an analog convolutional image sensor called RedEye that
    performs layers of a convolutional neural network in the analog domain
    before quantization. It aims to improve energy efficiency in continuous
    mobile vision. The paper gives both the hardware architecture and analog
    circuit design of RedEye. RedEye mitigates analog design complexity, using a
    modular column-parallel design to promote physical design reuse and
    algorithmic cyclic reuse. RedEye uses programmable mechanisms to admit noise
    for tunable energy reduction.

2.  The paper uses a simulation-based framework to estimate task accuracy and
    energy consumption. This allows developers to optimize their RedEye programs
    and noise parameters for minimal energy consumption at sufficient task
    accuracy.

3.  Compared to conventional systems, RedEye reports an 85% reduction in sensor
    energy, 73% reduction in cloudlet-based system energy, and a 45% reduction
    in computation-based system energy. RedEye advances towards overcoming the
    energy-efficiency barrier to continuous mobile vision. While they design and
    simulate RedEye energy, noise, and timing performance, they do not yet
    provide a circuit layout of the RedEye architecture.

**Lessons learnt:**

1.  To address analog readout bottleneck, the key idea of the paper is to push
    early processing into the analog domain to reduce the workload of the analog
    readout.

2.  RedEye positions a convergence of analog circuit design, systems
    architecture, and machine learning, which allows it to perform early
    operations in the image sensor’s analog domain, moving toward continuous
    mobile vision at ultra low power.
