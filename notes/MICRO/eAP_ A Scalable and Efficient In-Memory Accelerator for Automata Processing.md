**Paper title:**

eAP: A Scalable and Efficient In-Memory Accelerator for Automata Processing.

**Publication:**

MICRO’19

**Problem to solve:**

Existing in-memory automata processing accelerators suffer from inefficient
routing architectures. They are either incapable of efficiently place-and-route
a highly connected automaton or require an excessive amount of hardware
resources.

**Major contribution:**

1.  Accelerate state transition stage: a compact and low-overhead interconnect
    architecture that efficiently implements the state transition stage in
    automata processing.

2.  embedded Automata Processor:

    1.  exploiting subarray-level parallelism in memory

    2.  designing an optimal pipeline for state matching and state transition

    3.  compact interconnect architecture

    4.  choice of memory technology

They evaluate eAP on both 8T and 2T1D memory arrays. Overall, eAP_2T1D achieves
1.7×, 5.1×, and 210× better throughput per unit area over eAP_8T, CA, and the
AP, respectively, all in 28nm technology.

**Lessons learnt:**

Firstly, this paper reorganized the state transition stage’s interconnection. To
achieve this, Reduced Crossbar Interconnect were used to simplify the network.
Then they proposed different optimization schemes based on different memory
structure designs, and applied these schemes to the network structure design in
a targeted manner.

Secondly, the overall design of eAP architecture is shown in the papoer. Memory
bank supports two modes; normal mode (NM), for data storage as last-level cache,
and automata mode (AM). During the AM, the global decoder only selects one of
the connected subarrays based on the input address, and then selects one row
within the subarray. During the AM, all the local decoders get the same address
(input symbol) from the global decoder and activate the same row in each
subarray, in parallel, based on the input symbol. And the pipeline of eAP tries
to balance the amount of work between the two stages of the pipeline, since the
final frequency is determined based on the slowest stage.
