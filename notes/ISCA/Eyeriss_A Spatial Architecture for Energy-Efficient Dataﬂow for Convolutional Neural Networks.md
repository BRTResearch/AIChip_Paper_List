**Paper title:**

Eyeriss: A Spatial Architecture for Energy-Efficient Dataﬂow for Convolutional
Neural Networks

**Publication:**

ISCA’16

**Problem to solve:**

Although highly-parallel compute paradigms, such as SIMD/SIMT, effectively
address the computation requirement to achieve high throughput, energy
consumption still remains high as data movement can be more expensive than
computation. Accordingly, finding a dataﬂow that supports parallel processing
with minimal data movement cost is crucial to achieving energy-efficient CNN
processing without compromising accuracy.

**Major contribution:**

1.  A taxonomy that classifies existing CNN dataflows from previous research.

2.  A spatial architecture based on a new CNN dataflow, called row stationary,
    which is optimized for throughput and energy efficiency. This dataflow has
    been demonstrated on a fabricated chip.

3.  An analysis framework that can quantify the energy efficiency of different
    CNN dataflows under the same hardware constraints. It can also search for
    the most energy efficient mapping for each dataflow.

**Lessons learnt:**

The paper for the first time clarifies the CNN dataflow, i.e., row stationary
dataflow that optimizes for all types of data movement energy costs to achieve
energy efficiency.

Experiments using the CNN configurations of AlexNet show that the proposed RS
dataflow is more energy efficient than existing dataflows in both convolutional
(1.4× to 2.5×) and fully-connected layers (at least 1.3× for batch size larger
than 16). The RS dataflow has also been demonstrated on a fabricated chip, which
verifies the energy analysis.
