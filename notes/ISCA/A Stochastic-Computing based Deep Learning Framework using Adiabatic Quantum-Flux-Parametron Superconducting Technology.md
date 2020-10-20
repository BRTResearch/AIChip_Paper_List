**Paper title:**

A Stochastic-Computing based Deep Learning Framework using Adiabatic
Quantum-Flux-Parametron Superconducting Technology

**Publication:**

ISCA’19

**Problem to solve:**

Adiabatic Quantum Flux Parametron(AQFP) is a kind of superconducting technology.
It has much higher energy-efficiency than CMOS. Moreover, AQFP logic gate is
naturally deep piplined and can achieve true Random Number Generation(RNG) using
a single AQFP buffer, which is compatible with Stochastic Computing(SC). Thus,
the authors proposed a SC based DNN accelerator by using AQFP as fundamental
logic gate instead of CMOS.

**Major contribution:**

The SC based DNN architecture using AQFP. They investigate that the inner
prodect calculation in FC layers has more number of inputs than that in CONV
layers. And accurate activation function is critical in CONV layers. Thus,
bitonic sorting network and feadback loop used in CONV layer is more accurate
than majority chain in FC layers. They also propose:(1) a stochastic number
genaration(SNG)(2) a sub-sampling block(3)automatic buffer/splitter insertion.

A SNG is used to convert a binary number to its correspongding stochastic
format. This is achieved via comparing between the binary number (to convert)
with a stream of random numbers. 1-bit ture RNG can be implemented using 1 AQFP
logic gate. Thus, the authors use N× N RNG matrix to generate 4 N-bit random
number.

They propose an algorithm and implement in hardware to transform input-weight
products and bias into activated inner-product. On the way of achieving the
algorithm, they need bitonic sorter and bitonic merger.

Average-pooling block is similar as feature extraction block. The FC layer
architecture is simpler than CONV layer because of the lower require of
accuracy.

The authors implentment the accelerator in simulator(software) and real chip.
The proposed acccelerator can be up to 7.76 × 105 times more energy efficient
than CMOS implementation.
