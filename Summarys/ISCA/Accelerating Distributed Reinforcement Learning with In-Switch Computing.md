Corresponding author

Youjie Li, Iou-Jen Liu, Yifan Yuan, Deming Chen, Alexander Schwing, Jian Huang,
UIUC

Keywords

distributed machine learning, reinforcement learning, in-switch accelerator,
in-network computing

Summary

*Challenge*

The distributed RL training **generates orders of magnitude more iterations with
much smaller sized but more frequent gradient aggregations**. This is the major
bottleneck in distributed RL training which occupies up to 83.2% of the
execution time of each training iteration.

*Contribution*

1.  Propose iSwitch, an in-switch acceleration solution that moves the gradient
    aggregation from server nodes into the network switches.

2.  Rethink the distributed RL training algorithms and also propose a
    hierarchical aggregation mechanism to further increase the parallelism and
    scalability of the distributed RL training at rack scale

3.  Extend network protocol. To support in-switch computing for distributed RL
    training, they propose to build their own protocol and packet format based
    on regular network protocols.

4.  Implement iSwitch using a real-world programmable switch NetFPGA board and
    extend the control and data plane of the programmable switch to support
    iSwitch without affecting its regular network functions.

*Innovation Points*

The iSwitch conducts the in-switch aggregation at the granularity of network
packets rather than the entire gradient vectors (consisting of numerous network
packets).

*Result*

The accelerator support for both synchronous and asynchronous distributed RL
training with improved parallelism. Experiments show that iSwitch offers a
system-level speedup of up to 3.66× for synchronous distributed training, and
3.71× for asynchronous distributed training, compared with state-of-the-art
approaches.
