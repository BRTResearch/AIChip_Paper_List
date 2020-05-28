**Paper title:**

Interstellar: Using Halide’s Scheduling Language to Analyze DNN Accelerators

**Publication:**

ASPLOS‘20

**Problem to solve:**

To help understand and further improve the DNN accelerators, the space of all
accelerators can be formally specified by how they transform (block, reorder and
parallelize) the loop nest because all the hardware designs perform the same
computation, i.e., a seven-level loop nest for convolution. This paper uses this
insight to create a formal taxonomy of DNN accelerators that expresses design
choices as different loop transformations.

**Major contribution:**

1.  This paper introduces a systematic approach to precisely and concisely
    describe the design space of DNN accelerators as schedules of loop
    transformations.

2.  Shows that both the micro-architectures and dataflow mappings for existing
    DNN accelerators can be expressed as schedules of a Halide program, and
    extends the Halide schedule language and the Halide compiler to produce
    different hardware designs in the space of dense DNN accelerators.

3.  Creates a tool to optimize the memory hierarchy, which is more important
    than the choice of dataflow, achieving a 1.8X to 4.2X energy improvement for
    CNNs, LSTMs, and MLPs.

**Lessons learnt:**

Our results using Halide and the optimization framework show, with proper loop
blocking, many dataflow choices can achieve similar and close-to-optimal energy
efficiency. This large number of “optimal” solutions results from the fact that
operands in most convolutional layers in DNNs have high reuse rates so, as long
as properly blocked, most data references occur locally. Tailoring the loop
blocking to each architecture is key; the blocking approach is usually more
critical than the dataflow choice.
