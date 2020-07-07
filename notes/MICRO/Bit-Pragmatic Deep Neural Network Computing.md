**Paper title:**

Bit-Pragmatic Deep Neural Network Computing

**Publication:**

MICRO’17

**Problem to solve:**

With power limiting modern high-performance DNN accelerator, achieving better
energy efficiency is essential and can enable further advances.

The source of ineffectual computations in DNN accelerator is best understood in
the context of conventional multipliers which generate internally multiple
terms, that is, products of the multiplicand and powers of two, which added
together produce the final product. At runtime, many of these terms are zero as
they are generated when the multiplicand is combined with the zero-bits of the
multiplicator. While conventional bit-parallel multipliers calculate all terms
in parallel to reduce individual product latency, it still processes many
ineffectual neuron bits: Any time a zero bit is multiplied by a synapse it adds
nothing to the final output neuron. These ineffectual bits are introduced by the
conventional positional number representation. If these multiplications could be
avoided it would take even less time to calculate each product improving energy
and performance

**Major contribution:**

This work presents Pragmatic (PRA) a DNN accelerator whose goal is to process
only the essential (non-zero) bits of the input neuron. PRA exploits two sources
of ineffectual computations: 1) zero product terms which are the result of the
lack of explicitness in the multiplicator representation, and 2) the excess in
the representation precision used for both multiplicants and multiplicators.
Measurements demonstrate that for the convolutional layers, a straightforward
variant of PRA improves performance by 2.6x over the DaDiaNao (DaDN) accelerator
and by 1.4x over Stripes (STR). Similarly, PRA improves energy efficiency by 28%
and 10% on average compared to DaDN and STR. An improved cross lane
synchronization scheme boosts performance improvements to 3.1x over DaDN.
