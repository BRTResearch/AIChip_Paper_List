**Paper title:**

SpinalFlow: An Architecture and Dataflow Tailored for Spiking Neural Networks

**Publication:**

ISCA’20

**Problem to solve:**

The main contributions of this paper are:

-   An analysis of the inefficiencies in a baseline SNN design.

-   A representation for spike inputs and outputs that is compressed,
    time-stamped, and sorted.

-   **An SNN architecture and dataflow** that is tailored for this input/output
    representation and that increases reuse of neuron potential, input spikes,
    and weights.

-   A **1.8× average energy improvement** at 4-b resolution and **90% sparsity**
    over a 4-bit version of Eyeriss, a **5× average energy improvement** at 4-b
    resolution and 5.4× average latency improvement at a sparsity of 90% over
    8-bit Eyeriss, a 1.16× average energy improvement at a sparsity of 90% over
    an SCNN [46] baseline, and an order of magnitude energy improvement over the
    baseline SNN architecture.

The paper thus shows that SNN architectures can complete the computations
required for inference in similar time and energy as an ANN architecture. This
can significantly impact platforms, e.g., those requiring real-time learning,
where SNNs have the potential to achieve higher accuracies than ANNs.

**Lessons learnt:**

The authors transfer a typical accelerator architecture of CNN into SNN domain
as baseline, analysis the weakness of this baseline design, and correspondingly
propose an enhanced design.
