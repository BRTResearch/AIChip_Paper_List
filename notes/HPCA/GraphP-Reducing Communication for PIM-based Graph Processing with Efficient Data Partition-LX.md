**Paper title:**

GraphP: Reducing Communication for PIM-based Graph Processing with Efficient
Data Partition

**Publication:**

HPCA’18

**Problem to solve:**

In graph application, there are significant data movements. This posed great
challenges to conventional computer architecture and memory systems. It is
well-known for the poor locality in traversing the neighborhood vertices, and
high memory bandwidth requirement, because the computations on data accesses
from memory are typically simple.

**Major contribution:**

1.  This paper proposed GraphP, a novel HMC-based software/hardware co-designed
    graph processing system that drastically reduces communication and energy
    consumption compared to state-of-the-art system, TESSERACT.

2.  The first feature is “Source-cut” partitioning, which fundamentally changes
    the cross-cube communication from one remote put per cross-cube edge to one
    update per replica.

3.  The second feature is “Two-phase vertex program”, a programming model
    designed for “source-cut” partitioning with two operations: GenUpdate and
    ApplyUpdate.

4.  The third feature is “Hierarchical communication and overlapping”, which
    further improves performance with unique opportunities offered by the
    proposed partitioning and programming model.

**Lessons learnt:**

1.  Designing an architecture may start out data organization, not based on
    programming model. This is a heuristic-based design idea to improve
    performance.

2.  PIM is an effective technique that reduces data movements by integrating
    processing units within memory. Therefore, PIM can be employed into the NN
    fields and improve the speedup and energy saving.
