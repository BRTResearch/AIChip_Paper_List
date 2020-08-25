**Paper title:**

Understanding Reuse, Performance, and Hardware Cost of DNN Dataflow\_ A
Data-Centric Approach

**Publication:**

MICRO’19

**Problem to solve:**

1.  In deep learning accelerators, the microarchitecture of the accelerator is
    coupled with the dataflow of the layers. The selection on dataflow for a
    layer can have a large impact on utilization and energy efficiency.

2.  There is a lack of understanding on the choices and consequences of
    dataflows, and of tools and methodologies to help architects explore the
    co-optimization design space.

**Major contribution:**

1.  A data-centric notation to represent various accelerator dataflows with data
    mappings and reuses being first-class entities.

2.  Method of using the mentioned data-centric notation to analyze reusing in a
    structured manner.

3.  An analytical cost model named MAESTRO (Modeling Accelerator Efficiency via
    Spatio-Temporal Reuse and Occupancy) that programmatically implements the
    above analysis.

**Lessons learnt:**

This work is important for architecture researchers in deep learning domain. The
tool and the method produced by this paper can quickly help check your
architecture design.
