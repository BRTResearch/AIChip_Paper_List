**Paper title:**

Maximizing CNN Accelerator Efficiency Through Resource Partitioning

**Publication:**

ISCA’17

**Problem to solve:**

1.  Improvements in CNN accuracy are accompanied by a rapid increase in
    computational cost. CNNs have already grown to the point where multi-core
    CPUs are no longer a viable computing platform. At the same time, while GPUs
    offer adequate performance, GPU power consumption brings its own set of
    challenges, particularly at data-center scale. FPGAs have seen a surge in
    interest for CNN acceleration due to their programmable, massively parallel,
    and power-efficient computing substrate.

2.  We observe that jointly optimizing one CLP for all CNN layers leads to a
    dynamic underutilization of FPGA resources, giving up performance that could
    be achieved on the FPGA platform. Although the CLP is optimized for maximum
    throughput, the fixed dimensions of the computational grid are sub-optimal
    for some, or even all, of the individual layers.

**Major contribution:**

1.  we propose a new CNN accelerator design that partitions FPGA resources among
    multiple CLPs, which operate on multiple images concurrently. We illustrate
    the operation of Multi-CLP, where the hardware resources are partitioned
    among two smaller CLPs that operate in parallel on different images. Note
    that the two CLPs are specialized and have different dimensions; this allows
    CLP1 to work well for L1 and L3, while CLP2’s dimensions are compatible with
    L2. The key is that these sizes allow the layers to be processed with very
    little idle hardware, enabling the Multi-CLP to do the same amount of work
    in less time.

2.  We develop an optimization algorithm that, given CNN layer dimensions and a
    resource budget, computes a partitioning of the FPGA resources into multiple
    CLPs for an efficient high-performance design. Our algorithm runs in minutes
    and produces a set of CLP dimensions. We then use these dimensions to
    parameterize a CLP design specified using high-level synthesis (HLS),
    combining the resulting CLPs to form a complete CNN implementation..

3.  Our results demonstrate that partitioning FPGA resources into multiple CLPs
    can achieve over 90% arithmetic unit utilization, in some cases close to
    100%. Our design methodology achieves 3.8x higher throughput than the
    state-of-the-art approach for the popular AlexNet CNN on a Xilinx Virtex-7
    FPGA. For the more recent SqueezeNet and GoogLeNet, the speedups are 2.2x
    and 2.0x.
