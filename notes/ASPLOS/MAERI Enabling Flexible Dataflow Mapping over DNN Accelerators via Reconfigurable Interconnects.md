**Paper title:**

MAERI Enabling Flexible Dataflow Mapping over DNN Accelerators via
Reconfigurable Interconnects

**Publication:**

ASPLOS‘18

**Problem to solve:**

Most DNN accelerators support only fixed dataflow patterns internally as they
perform a careful codesign of the PEs and the NoC. The majority of them are only
optimized for traffic within a convolutional layer. This makes it challenging to
map arbitrary dataflows on the fabric efficiency, and can lead to
underutilization of the available computer resources.

**Major Contributions:**

1.  Present MAERI (Multiply-Accumulate Engine with Reconfigurable Interconnect),
    which is a DNN accelerator built with a set of modular and configurable
    building blocks that can easily support myriad DNN partitions and mappings
    by appropriately configuring tiny switches. It is not only capable of
    running CONV, LSTM, POOL and FC layers, but also supports cross-layer
    mapping and sparsity.

2.  Evaluate MAERI which provides 8-459% better utilization across multiple
    dataflow mappings over baselines with rigid NoC fabrics while adding 6.5%
    power overhead and reducing 36.8% area overhead over a state-of-the-art
    baseline like Eyeriss, and adding 47.0% area and increase throughput by
    49.0% over a systolic array.
