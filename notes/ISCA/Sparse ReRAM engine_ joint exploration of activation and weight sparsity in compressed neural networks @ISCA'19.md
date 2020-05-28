**Paper title:**

Sparse ReRAM engine: joint exploration of activation and weight sparsity in
compressed neural networks

**Publication:**

ISCA’19

**Problem to solve:**

Exploiting the sparsity for ReRAM-based NN accelerator to achieve energy
efficiency for DNN inference accelerators.

This paper points out that existing architectural studies on ReRAM-based NN
accelerators assume that an entire crossbar array can be activated in a single
cycle. However, due to inference accuracy considerations, matrix-vector
computation must be conducted in a smaller granularity in practice, leading much
lower parallelism than that was assumed in prior ReRAM-based NN accelerators.

This paper proposes the first practical Sparse ReRAM Engine (SRE) that exploits
both weight and activation sparsity. Based on some statistics from fabrication
studies, this paper proposes much smaller granularity of parallelism in ReRAM
crossbar, called Operation Unit (OU), but leverages the sparsity for
optimization. Evaluation results show that, for neural networks that use the
structural pruning algorithm to regularize weight sparsity during training, SRE
provides up to 42.3x performance speedups (average 13.1x) and up to 95.4% energy
savings (average 85.3%) over a baseline that does not exploit sparsity.

**Major contribution:**

-   The authors claim that they are the first sparsity exploration work that
    targets a practical hardware design for ReRAM-based accelerators instead of
    an over-idealized architecture. And they show that a practical OU-based
    design enables new opportunities to effectively exploit DNN sparsity.

-   They propose a SRE to jointly exploit weight and activation sparsity, with
    only minimal indexing overhead. They take advantage of fine-grained OU-based
    computations and combines row-wise weight compression with dynamic wordline
    activation to provide significant performance speedup and energy savings.

-   They show that SRE enables a practical ReRAM-based DNN accelerator design,
    which achieves satisfactory inference accuracy considering the limitation of
    ReRAM cell reliability while delivering comparable performance and energy
    efficiency with the over-idealized ReRAM DNN accelerator.

**Lessons learnt:**

ReRAM-based NN accelerator are being over-idealized in the past studies, and
this study makes the first attempt to bring us back to the reality from
architecture perspective by leveraging sparsity for optimization.
