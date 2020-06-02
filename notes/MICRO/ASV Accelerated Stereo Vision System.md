**Paper title:**

ASV: Accelerated Stereo Vision System

**Publication:**

MICRO’19

**Problem to solve:**

The demand for intelligent applications running on a diverse range of mobile and
embedded platforms, such as micro-robots, augmented reality headsets, and
smart-city sensor nodes, shows no sign of slowing down. A key primitive in these
applications is estimating depth information from the environment, which in turn
serves as the building block for extracting higher-level semantics. For
instance, depth information enables a mobile robot to detect and manipulate
objects that are in close proximity.

**Major contribution**

Propose the first stereo vision algorithm, ISM, that exploits temporal
invariance in stereo imaging to improve the performance with minimal accuracy
loss;

Propose the first static optimization framework for deconvolution, a key
operation in stereo DNNs, which eliminates the sparsity-induced compute
inefficiencies in deconvolution layers without hardware changes;

The first to identify inter-layer activation reuse in deconvolution, a unique
data reuse opportunity exposed by the proposed transformation framework, and
which uses an efficient constrained optimizer.

Co-design the hardware with the proposed software optimizations to achieve fast,
low-power stereo vision with minimal changes to existing DNN accelerators.

**Lessons learnt**

Given an image pair, stereo matching algorithms first generate the disparity
map, from which depth is then calculated through triangulation.

The ISM algorithm obtains correspondences in key frames using DNNs, and
propagates the correspondences to non-key frames to guide the cheap
correspondence search.
