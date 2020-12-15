**Paper title:**

High-Performance Deep-Learning Coprocessor Integrated into x86 SoC with
Server-Class CPUs

**Publication:**

ISCA’2020

**Problem to solve:**

1.  Existing technologies leave a large gap in DL hardware solutions with regard
    to performance, cost and form factor. Many established semiconductor
    companies and startups are striving to design new inference hardware to fill
    this market gap. However, developing a high performance, low cost, small
    form factor DL accelerator has a high barrier to entry.

2.  Centaur Technology’s unique position to leverage existing infrastructure,
    in-house x86 designs, expert engineers, and regular development and
    fabrication cycles removes many barriers to the DL inference hardware space.
    This position caters to Centaur’s historical design goals of adding high
    value to its low-cost offerings.

**Major contribution:**

1.  This paper describes Centaur’s 20 teraoperations-per-second DL coprocessor
    technology (Ncore), integrated with eight 64-bit x86 CPUs utilizing
    Centaur’s new CNS microarchitecture into a single SoC platform (called CHA).
    CHA is the industry’s first x86 SoC with integrated high-performance DL
    coprocessor and server-class CPUs.

2.  We show that the inference hardware arena is prime for Centaur’s entry by
    demonstrating a full hardware and software solution delivered with minimal
    risk, high-performance, and small form factor. This solution has been
    deployed in third party video analytics prototypes, as well as in
    engineering development platforms internally.

3.  Ncore’s latencies beat those of established DL giants in the MLPerf
    Inference v0.5 Closed-division benchmark, while also providing high
    throughput and multifaceted flexibility. CHA’s integration of both x86 and
    Ncore can flexibly support everchanging DL models and can further expand
    performance capabilities through multi-socket, multi-system, and
    multiexpansion card solutions as desired.

**Lessons learnt:**

While the software stack presented here scheduled and optimized x86 and Ncore
operations independently, MLIR is an exciting new project that explores a
unified compiler framework for heterogeneous hardware . They are exploring ways
to leverage MLIR to provide a unified compiler stack for co-optimizing the
scheduling and code-generation between x86 and Ncore in order to increase
concurrency and further leverage the availability of x86 cores.
