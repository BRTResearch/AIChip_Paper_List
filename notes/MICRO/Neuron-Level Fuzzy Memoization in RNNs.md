**Paper title:**

Neuron-Level Fuzzy Memoization in RNNs

**Publication:**

MICRO’19

**Problem to solve:**

For recurrent neural network, this paper found that the output of RNN’s neuron
exhibits small changes in consecutive invocations. This paper exploits this
property to build a memory scheme to avoid the repeating computation and improve
the computing speed.

**Major contribution:**

1.  This paper provided an evaluation of the outputs of neurons in recurrent
    layers, and show that they exhibit small changes in consecutive executions.

2.  This paper proposes a fuzzy memorization scheme that avoid more than 24.2%
    of neuron evaluations by reusing previously computed results stored in a
    memorization buffer.

3.  This paper proposed the use of a BNN to determine when memorization can be
    applied with small impact on accuracy. It also showed that BNN and RNN
    outputs are highly correlated.

4.  This paper also implemented the neuron-level memorization scheme on top of a
    state-of-the-art RNN accelerator. It provided 1.35x speedup and 18.5% energy
    savings on average for several RNNs.

**Lessons learnt:**

1.  It is essential to analyze the detail of a data-processing algorithm and
    identify the stable regularity, such as reusability of per-step results.
    This may be an idea to find a valuable problem.

2.  Employing Binarized Neural Network (BNN) reasonably in architecture
    designing is an effective and creative way. Because BNN is extremely small,
    hardware-friendly and very effective at predicting when memorization can be
    safely applied.

3.  The key to accelerating large-scale data process is to exhibit the trade-off
    between reusing and repeating in a view of little output error. Therefore,
    the threshold may a good tool to help us to be available to reach a
    promising balance.
