**Paper title:**

Bit Fusion: Bit-Level Dynamically Composable Architecture for Accelerating Deep
Neural Network

**Publication:**

ISCA’2018

**Problem to solve:**

1.  A fixed-bitwidth accelerator would either offer limited benefits to
    accommodate the worst-case bitwidth requirements, or inevitably lead to a
    degradation in final accuracy.

2.  The algorithmic properties of DNNs have not fully been utilized to push the
    envelope on their acceleration efficiency and performance. There are three
    properties can be used to improve acceleration: (1) DNNs are mostly a
    collection of massively parallel multiply-adds; (2) The bitwidth of these
    operations can be reduced with no loss in accuracy; (3) to preserve
    accuracy, the bitwidth varies significantly across DNNs and may even be
    adjusted for each layer individually

3.  Some architectures, such as Stripes and UNPU, have the similar struct, but
    they fix the bitwidth of one operand and support variable bitwidths for the
    other.

**Major contribution:**

1.  An innovative microarchitecture, called BitBricks, for multiply-add
    operations is proposed to support variable bitwidths operations and it can
    provide a concise expression for a wide range of DNN including CNN, RNN,
    etc.

2.  To energy saving, the structure Bit Fusion, composed with some BitBricks,
    augments the input and weigh buffers with a register which holds a row of
    data that is gradually fed the Fused-PEs. So that, at each cycle, the
    systolic array will consume a vector of inputs and matrix to produce a
    vector of outputs with fewest accessed to the buffers and the minimal
    bitwidth possible.

3.  The properties of DNNs and a mathematical property that a multiply operation
    between operands with power-of-2 bitwidths can be decomposed to 2-bit
    multiplications. Then the products can be put together by shifted-add
    operations (shown in Fig.1).

4.  To satisfy the dynamically fuse to match the bitwidth of individual DNN
    layers, the architecture can be designed to the assembly of the same module
    like author’s BitBricks. The modules , BitBricks, are arranged for different
    structures to match the input bitwitdhs. And this flexibility in the
    architecture enables minimizing the computation and the communication at the
    finest granularity possible with no loss in accuracy.
