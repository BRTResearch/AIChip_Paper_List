**Paper title:**

Prague: High-Performance Heterogeneity-Aware Asynchronous Decentralized Training

**Publication:**

ASPLOS’2020

**Problem to solve:**

1.  Distributed deep learning training usually adopts All-Reduce as the
    synchronization mechanism for data parallel algorithms due to its high
    performance in homogeneous environment. However, its performance is bounded
    by the slowest worker among all workers.

2.  The first key challenge of distributed training is the intensive
    communication among workers. During execution, gradients or parameter
    updates are transferred among workers in different nodes to achieve the
    eventually trained model. In PS, all workers need to communicate with the
    parameter servers — easily causing communication bottleneck even if the
    number of workers is relatively small. In All-Reduce, the communication is
    more evenly distributed among all workers, but since it logically implements
    all-to-all communication, the amount of parameters transferred is still
    large. More importantly, to hide communication latency, All Reduce uses
    delicate pipelined operations among all workers. It makes this solution
    vulnerable to system heterogeneity.

3.  because All-Reduce requires global synchronization in every step, its
    performance is bounded by the slowest worker, thereby cannot tolerate
    heterogeneity well. We believe that heterogeneity is the second key
    challenge of distributed training.

**Major contribution:**

1.  we propose Prague, a high-performance heterogeneity-aware asynchronous
    decentralized training approach. Compared to the state-of-the-art solutions,
    Prague gets the best of both worlds: it achieves better performance than
    All-Reduce even in homogeneous environment and significantly outperforms
    AD-PSGD in both homogeneous and heterogeneous environments.

2.  To reduce synchronization cost, we propose a novel communication primitive,
    Partial All-Reduce, that enables fast synchronization among a group of
    workers. To reduce serialization cost, we propose static group scheduling in
    homogeneous environment and simple but smart techniques, i.e., Group Buffer
    and Group Division, to largely eliminate conflicts with slightly reduced
    randomness.

**Lessons learnt:**

This paper focuses on the problems of homogeneous and heterogeneity tolerance in
distributed training. The traditional PS and All-Reduce method has advantages
and disadvantages, but it cannot achieve the performance that is comparable to
All-Reduce in a homogeneous environment while still maintaining superior ability
to tolerate heterogeneity.
