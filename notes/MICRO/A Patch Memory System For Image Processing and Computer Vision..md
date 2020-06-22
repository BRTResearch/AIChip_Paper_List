**Paper title:**

A Patch Memory System For Image Processing and Computer Vision

**Publication:**

MICRO’16

**Problem to solve:**

In image processing and computer vision domain, ability to process large volumes
of data is required. And the data are often 2D or 3D addressed, so the common
memory system of the computation units like cache, are lack of the
characteristic of 2D and 3D, resulting the extra overhead in data load and
write. This paper tries to solve this problem in image process and computer
vision.

**Major contribution:**

A memory system called ‘PMEM’ that: supporting 2D and 3D addressing; providing
multidimensional data primitives; Optimizing the ‘patch’ operation by special
hardware design; providing automatic halo handle.

**Lessons learnt:**

The method in this paper targets image processing domains. First, this kind of
system requires the whole support from program model level to hardware level,
and that is not easy, especially the benefit is not that large as other
optimizing methods. However, this paper provides a full vision of memory system
design for domain-specific computing.
