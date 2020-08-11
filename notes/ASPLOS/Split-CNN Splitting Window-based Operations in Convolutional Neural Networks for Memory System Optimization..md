**Paper title:**

Split-CNN: Splitting Window-based Operations in Convolutional Neural Networks
for Memory System Optimization.

**Publication:**

ASPLOS’19

**Problem to solve:**

The memory requirements of deep convolutional neural networks are growing
increasingly. Unfortunately, today’s GPUs have considerably small device memory.
Since the trend of deep learning is toward deeper and larger networks, the
bottleneck on the GPU’s memory capacity will only become worse and must be
overcome. Specifically, there are three challenging trends contributing to the
memory bottleneck of training deep neural networks: prevalence of memory-bound
layers, increasing batch sizes, and increasing model complexity.

**Major contribution:**

To tackle above problems, the paper mainly makes three contributions as follows:

1.  proposes Split-CNN, a generic instrumentation of the regular CNN models,
    that breaks apart memory bottlenecks of the CNN models while retaining or
    even enhancing the application-specific metrics of the model (i.e.,
    classification accuracy).

2.  introduces a new heterogeneous memory management system (HMMS) to optimally
    schedule memory allocation, deallocation, offloading and prefetching without
    any required tuning on the network models.

3.  combines Split-CNN and HMMS to showcase that Split-CNN can be trained with
    significantly larger batch size, thus effectively solving the challenges
    with the increasing demands on large batch size.

**Lessons learnt:**

Based on the analysis, Split-CNN achieves 2.1x speedup in the distributed
training for VGG-19 model with typical cloud network bandwidth. The paper
demonstrates the effectiveness of the proposed solutions to the first two
challenges, and the authors envision that deep learning application developers
working with models with high complexities will be able to utilize their
techniques to solve the third challenge as they face it.
