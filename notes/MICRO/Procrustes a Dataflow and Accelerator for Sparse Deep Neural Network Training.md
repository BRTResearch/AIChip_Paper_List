**Paper title:**

Procrustes: a Dataflow and Accelerator for Sparse Deep Neural Network Training

**Publication:**

MICRO’2020

**Problem to solve:**

Pruned DNN models with sparse weight has been used to save energy and time. In
previous sparse DNN works, a model is first trained with the full parameter set,
then pruned, and finally re-trained to recover accuracy. But in the paper it is
argued that skipping the pre-training step is not an option.

Ideally, sparse-from-scratch training can offer significant savings. But
existing sparse training methods either takes too much to sort the weights or
suffer accuracy loss. A new design that accelerate sparse training is needed.

**Major contribution:**

The contribution of Procrustes can be separated as three parts:

1.  Sparse training considerations: the paper focuses on Dropback algorithm and
    solves two main problems of it. Dropback algorithm does not set pruned
    weights to zero, which cannot save MAC energy. Procrustes examined whether
    the initial weight values could be gradually decayed to zero and finally
    zeroed them. Also, Procrustes replaces the target sparsity factor with a
    global value threshold θ.

2.  Dataflow & sparse data format: A sparse weight storage format is introduced.
    Procrustes uses a modified compressed sparse block (CSB) format to store
    weights in the on-chip, global buffer and external DRAM. Also, Procrustes
    cut work tiles into halves to do load balancing.

3.  Hardware architecture: The paper gives the architecture structure of
    Procrustes.
