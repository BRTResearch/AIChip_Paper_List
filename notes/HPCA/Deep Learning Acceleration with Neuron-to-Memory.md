**Paper title:**

Deep Learning Acceleration with Neuron-to-Memory Transformation

**Publication:**

HPCA’ 20

**Problem to solve:**

Although many DNN models are implemented on high-performance computing
architectures such as GPGPUs by parallelizing tasks, running neural networks on
the general purpose processors is still slow, energy-hungry, and prohibitively
expensive. Earlier work proposed FPGAs and ASIC designs to accelerate neural
networks. However, these techniques pose a critical technical challenge due to
data movement cost. Processing in-memory (PIM) is a promising solution to
address the data movement issue by implementing logics within a memory. Although
memristor array approaches are the first pace towards employing PIM for DNN
acceleration, they have three significant downsides: (i) They utilize Analog to
Digital Converters (ADCs) and Digital to Analog Converters (DACs) which take the
majority of the chip area and power consumption, e.g., 98% of chip area in DNN
accelerator. In addition, the mixed-signal ADC/DAC blocks do not scale as fast
as the memory device technology does. (ii) The existing PIM approaches use
multi-level memristor devices that are not sufficiently reliable for
commercialization unlike commonly-used single-level NVMs. (iii) Finally, they
only support matrix multiplication in analog memory while other operations such
as activation functions are implemented using CMOS-based digital logic. This
makes the design non-generic and increases the expense of fabrication.

The paper aims to propose a PIM accelerator accelerating DNN in a highly
parallel architecture to overcome the above-mentioned problems

**Major contribution:**

The paper use associative memory (AM) to build the DNN accelerator RAPIDNN. The
main contribution is as follow:

1.  Proposing a neuron-to-memory transform, analyzes computation flows of a DNN
    model, i.e. weighted accumulation, activation functions and encoding, and
    implement them with associative memory blocks. The paper uses clustering
    algorithms and other approximation to perform these operations in distinct
    space (i.e. using non-uniform quantization in extremely low bits, e.g. 2
    bits for both input and activation) with minimal accuracy loss.

2.  Presenting software support and adjustable DNN reinterpretation mechanisms
    that allow users to configure RAPIDNN for different DNN applications
    optimally. Impaction of different memory sizes on the inference accuracy are
    also explored.

3.  Proof-of-concept evaluations on six DNN applications demonstrate that using
    small-sized memory blocks, e.g., around 5 KB for each neuron, RAPIDNN can
    provide the same level of the prediction quality.

The paper argues that operations in DNN can be performed in extremely low bits
quantization, e.g. 2bits for both inputs, then such operations can be modeled as
lookup tables with $$2^{2 \times 2} = 16$$ items. Such lookup tables can be
easily implemented using associative memory blocks. The weights are quantized
using clustering algorithms, and the inputs quantization parameters are decided
by using k-means on the training dataset.

The paper also discusses the Nearest Distance CAM, which can find the item most
nearest to the input in absolute distance rather than hamming distance. Such
NSCAM are critical to support the weighted accumulation operations.

**Lessons learnt:**

The paper shows a new kind of PIM designs, i.e. using associative memory. The
transform from floating point operations to lookup tables containing very
limited items is inspiring and understandable.

The paper also solves the critical problem of finding nearest items in CAM using
absolute distance.
