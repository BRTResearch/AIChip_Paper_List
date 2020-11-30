**Paper title:**

Look-Up Table based Energy Efficient Processing in Cache Support for Neural
Network Acceleration

**Publication:**

MICRO’20

**Problem to solve:**

1.  Most of the existing state-of-the art SRAM based PIM designs perform
    computation by asserting multiple rows of memory to establish data-dependent
    bitline discharge. This technique is used in conjunction with modified sense
    amplifiers or the augmentation of digital logic at the edge of the SRAM
    array to perform various logical functions within an array.

2.  While such bitline computing offers potential for enormous parallelism in
    computing across all columns of a large cache, it imposes significant energy
    consumption involved with charging and discharging the bitlines. This
    overhead can become excessive for complex operations of DNN workloads that
    need to be broken down into a large sequence of simple bitline operations.

**Major contribution:**

1.  This paper present a bitline computation free PIM architectur (BFree)
    capable of computing various complex neural network primitives at the
    subarray granularity.

2.  BFree transforms the subarray into a LUT-based compute engine and makes use
    of a tiny PIM controller named BFree compute engine (BCE).

3.  This work enable the systolic data movement strategies for the matrix
    multiply and MAC-based operations within the memory which leads to further
    improvement in performance by overlapping computation with input load time.
