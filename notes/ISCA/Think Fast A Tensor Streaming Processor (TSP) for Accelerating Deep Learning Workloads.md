**Paper title:**

Think Fast: A Tensor Streaming Processor (TSP) for Accelerating Deep Learning
Workloads

**Publication:**

ISCA’20

**Problem to solve:**

The Tensor Streaming Processor (TSP) is built based on two key observations: (1)
machine learning workloads exhibit abundant data parallelism, which can be
readily mapped to tensors in hardware, and (2) a simple and deterministic
processor with producer-consumer stream programming model enables precise
reasoning and control of hardware components, achieving good performance and
power efficiency. The TSP is designed to exploit parallelism inherent in
machine-learning workloads including instruction-level, memory concurrency, data
and model parallelism, while guaranteeing determinism by eliminating all
reactive elements in the hardware.

In contrast from conventional multicore, where each tile is a heterogeneous
collection of functional units but globally homogeneous, the TSP inverts that
and they have local functional homogeneity but chip-wide (global) heterogeneity.

**Major contribution:**

1.  **Functional slicing**

The TSP reorganizes the homogeneous two-dimensional mesh of cores into the
functionally sliced microarchitecture. In this approach, each tile implements a
specific function and is stacked vertically into a “slice” in the Y-dimension of
the 2D on-chip mesh. They disaggregate the basic elements of a core. In this
organization, each functional slice is independently controlled by a sequence of
instructions specific to its on-chip role. For instance, the MEM slices support
Read and Write but not Add or Mul, which are only in arithmetic functional
slices (the VXM and MXM slices).

All of a slice’s tiles execute the same instruction stream (SIMD), so they can
factor out the common instruction decode and dispatch logic into its own tile
(ICU) and decompose the normal instruction execution pipeline into two areas:
(i) instruction fetch, decode, and parceling and (ii) operand read, execute, and
writeback. This approach decouples the memory subsystem from the functional
units retrieving their operands and depositing results.

1.  **Parallel lanes and streams**

In the TSP model, instructions flow Northward from the ICUs to the functional
slices, while data (operands and results) flow East and West between functional
slices. Any inter-lane data movement within a vector uses the on-chip network
(SXM) slice.

Conceptually, the functional slices are fixed and data is flowing across their
processing elements as shown in Figure 2. As the data flows through the slice,
each functional unit can optionally intercept the data operands and compute a
result (if its a processing element like an ALU), or move data between lanes on
the network if its a switching element.

Streams provide a programming abstraction and are a conduit through which data
flows between functional slices. Unlike GPRs, the functional slices operate on
streams of parallel data flowing East orWest across chip. The horizontally
flowing streams carrying operands intercept the vertically (Northward) flowing
instructions to perform a computation on a functional slice. The compiler
precisely tracks the chip’s architectural state and uses that knowledge to
ensure that instructions correctly intercept its stream operand(s).

Streams are implemented in hardware by a chip-wide streaming register file (SR).
They are architecturally-visible and transport operands and results between
slices. A common software pattern involves reading operand data from one or more
MEM slices that is then subsequently consumed and operated on by a downstream
arithmetic slice. The results of the operation are then produced onto another
stream such that they can be written back to memory.
