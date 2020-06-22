**Paper title:**

PM3: Power Modeling and Power Management for Processing-in-Memory

**Publication:**

HPCA’18

**Problem to solve:**

When the Processing-in-Memory (PIM) is prevalent in accelerating data-intensive
application, there are two problem becoming more and more severe in PIM
application. Firstly, the power consumption at the ideal peak throughput in
previous PIM designs may exceed its power supply beyond the DRAM thermal
tolerance capability with passive heat sink, which may have potential power
supply failure and memory reliability problems. Secondly, the power supply is
not fully utilized in this case. Therefore, it is important to have a
comprehensive quantitative study of the power modeling and power management for
such PIM architectures.

**Major contribution:**

1.  This paper models the relationship between bandwidth and power consumption,
    to facilitate early stage PIM power system designs, and then proposed the
    Power-Aware Subtask Throttling(PAST) technique to reduce PIM power
    requirement.

2.  This paper proposes the Processing-Unit Boost (PUB) technique based on a
    greedy algorithm, to improve the performance of processing units, and the
    Power Sprinting (PS) technique to improve the energy efficiency when the
    power supply is dynamically adapted.

3.  This paper proposes evaluating both HMC-based and RRAM-based PIM designs for
    their targeted applications. Also, via evaluations it demonstrated that NVMs
    and 3D DRAM have their own advantages in different bandwidth usage cases to
    be selected as PIM memories.

**Lessons learnt:**

1.  Dynamic power management may provide an insight into improving the energy
    efficiency and performance. Ideal method to consume the power is to put
    every drop of power on the crucial point and break the power wall. However,
    this is hard to target. So checking out the main bottleneck in a system
    comes with gains, and then design a scheme to address problem depending on
    this bottleneck model. This may be based on that domain-specific power
    consuming law, that is, there is a similar distribution of power usage
    within a field. That may be an interesting direction.

2.  To address the challenges in power management, let the system be aware of
    the power consuming throttling is an effective way to provide the points to
    optimize the performance.
