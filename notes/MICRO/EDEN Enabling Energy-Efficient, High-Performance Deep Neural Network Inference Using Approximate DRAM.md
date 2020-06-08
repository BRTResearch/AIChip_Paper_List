**Paper title:**

EDEN: Enabling Energy-Efficient, High-Performance Deep Neural Network Inference
Using Approximate DRAM

**Publication:**

MICRO’19

**Problem to solve:**

1.  DRAM has high energy consumption. Prior works on DNN accelerators report
    that between 30 to 80% of system energy is consumed by DRAM;

2.  DRAM has high latency. Prior work in accelerator design has targeted DRAM
    latency as a challenge for sparse and irregular DNN inference.

**Major contribution:**

1.  Approximate DRAM: the first general framework that increases the energy
    efficiency and performance of DNN inference by using approximate DRAM that
    operates with reduced voltage and latency parameters at the expense of
    reliability;

2.  Retain DNN accuracy methodology: To achieve this, EDEN basically use three
    steps: 1) EDEN improves the error tolerance of the target DNN by retraining
    the DNN using the error characteristics of the approximate DRAM module; 2)
    EDEN profiles the improved DNN to identify the error tolerance levels of all
    DNN data; 3) EDEN maps different DNN data to different DRAM partitions that
    best fit each datum’s characteristics, and accordingly selects the voltage
    and latency parameters to operate each DRAM partition

3.  Result: For a target accuracy within 1% of the original DNN, the results
    show that EDEN enables 1) an average DRAM energy reduction of 21%, 37%, 31%,
    and 32% in CPU, GPU, and two different DNN accelerator architectures,
    respectively, across a variety of state-of-the-art networks, and 2) an
    average (maximum) speedup of 8% (17%) and 2.7% (5.5%) in CPU and GPU
    architectures, respectively, when evaluating latency-bound neural networks.

**Lessons learnt:**

This paper mainly considered reducing hardware power consumption, in exchange
for power consumption at the expense of the accuracy of the hardware. Then use
the neural network's tolerance for errors to fix the error. This idea takes
advantage of the software in exchange for the performance of the hardware, and
the properties of the hardware can be configured according to different
workloads. But the problem is that the early calculation cost of the wrong model
is still relatively large, and the network needs to be retrained at the same
time, and the universality for different networks will be worse. Each
application of a different network model requires recalculation and
configuration.
