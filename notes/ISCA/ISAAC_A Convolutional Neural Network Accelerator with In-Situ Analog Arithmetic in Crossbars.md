**Paper title:**

ISAAC: a convolutional neural network accelerator with in-situ analog arithmetic
in crossbars

**Publication:**

ISCA’16

**Problem to solve:**

Put forward the ReRAM based architecture that supports DNN acceleration. It is
among the first pioneers that sheds light on this problem.

**Major contribution:**

1.  design a pipelined ReRAM architecture, with crossbars dedicated for each
    neural network layer, and eDRAM buffers that aggregate data between pipeline
    stages.

2.  define new data encoding techniques that are amenable to analog computations
    and that can reduce the high overheads of analog-to-digital conversion
    (ADC).

3.  define the many supporting digital components required in an analog CNN
    accelerator and carry out a design space exploration to identify the best
    balance of memristor storage/compute, ADCs, and eDRAM storage on a chip.

**Lessons learnt:**

This paper for the first time designs a full-fledged accelerator based on ReRAM
crossbars, and bit encoding schemes to deliver high throughput and manage the
high overheads of ADCs, DACs, and eDRAMs. This paper, together with PRIME,
proves the first architecture study for ReRAM based DNN inference accelerator.
