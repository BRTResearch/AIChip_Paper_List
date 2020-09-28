**Paper title:**

PROMISE An End-to-End Design of a Programmable Mixed-Signal Accelerator for
Machine- Learning Algorithms

**Publication:**

ISCA‘18

**Problem to solve:**

Analog/mixed-signal ML accelerators lack programmability, and even instruction
set interfaces, to support diverse ML algorithms or to enable essential software
control over the energy-vs-accuracy tradeoffs.

**Major Contributions:**

Propose PROMISE, the first end-to-end design of a PROgrammable MIxed-Signal
accElerator from Instruction Set Architecture (ISA) to high-level language
compiler for acceleration of diverse ML algorithms.

1.  Propose an ISA with a PROMISE architecture built with silicon-validated
    components for mixed-signal operations.

2.  Develop a compiler that can take a ML algorithm described in a high-level
    programming language (Julia) and generate PROMISE code, with an IR design
    that is both language-neutral and abstracts away unnecessary hardware
    details.

3.  Show how the compiler can map an application-level error tolerance
    specification for neural network applications down to low-level hardware
    parameters (swing voltages for each application Task) to minimize energy
    consumption.

4.  Carry on experiments which show that PROMISE can accelerate diverse ML
    algorithms with energy efficiency competitive even with fixed-function
    digital ASICs for specific ML algorithms, and the compiler optimization
    achieves significant additional energy savings even for only 1% extra
    errors.
