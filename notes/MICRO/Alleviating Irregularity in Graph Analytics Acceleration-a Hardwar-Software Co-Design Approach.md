**Paper title:**

Alleviating Irregularity in Graph Analytics Acceleration: a Hardware/Software
Co-Design Approach

**Publication:**

MICRO’19

**Problem to solve:**

With regard to graph analytics, accelerations for processing is a long-term aim
with lots of parallelisms found and then enhancing the implementation. While
more parallel processing at algorithm level, more irregularities occurs
alongside with computing and memory to hinder the presence of efficient
architecture design. Of these, the workload irregularity, traversal
irregularity, and update irregularity are the primary aspects needing
alleviating. If an architecture considers these three black points, it may
improve the speedup and energy-saving for graph analytics.

**Major contribution:**

1.  This paper proposed Dispatching/Processing programming model and the
    accelerator architecture to decouple the microarchitecture datapath for data
    dependency extraction at runtime.

2.  This paper proposes data-aware dynamic scheduling considering data
    dependencies, which elaborately schedules program on the fly, effectively
    tackling all three types of irregularities.

3.  This paper implements GraphDynS in RTL and evaluate it using a detailed
    microarchitectural simulation. Our comprehensive evaluations involve five
    well-known graph analytics algorithms with six large real-world graphs and
    five synthetic graphs. Compared to a state-of-the-art GPGPU-based solution,
    GraphDynS achieves 4.4× speedup and 11.6× less energy on average with half
    the memory bandwidth. Compared to a state-of-the-art graph analytics
    accelerator, GraphDynS achieves 1.9× speedup and 1.8× less energy on average
    with the same memory bandwidth.

**Lessons learnt:**

1.  Something with dynamic is presented again in architecture designing. Just in
    this paper, scheduling dynamically is utilized to maximize parallelism. The
    essence of dynamic operations is to execute some operation at the right
    time. Thereby, when faced with a new topic, find the non-dynamic process and
    consider that if dynamic process would be helpful to bring benefit for
    architecture design.

2.  Another interesting point is data-aware introducing. This may enlighten us
    that something-aware will make sense in diverse directions, similar to
    locality-ware, bandwidth-aware, computation-aware, searching-aware,
    partition-aware, model-aware, error-aware, system-aware, and so on.
    Something-aware is to find optimal way to occupy computing resource
    according to the limitation of computing. But find a solution is still
    challenging.

3.  Last but not least, decoupling a notion from a computer world could inspire
    some clear insight into optimization direction. This paper decoupled the
    datapath to assign data dependence for eliminating workload irregularities.
