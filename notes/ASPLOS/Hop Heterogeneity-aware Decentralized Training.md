**Paper title:**

Hop: Heterogeneity-aware Decentralized Training

**Publication:**

ASPLOS’19

**Problem to solve:**

1.Performance bottleneck in distributed training largely comes from two sources:
a) communication hotspot, especially for the PS — all workers need to put/get
updates to/from the PS; and b) heterogeneity, which causes fast workers to wait
for slow ones during synchronization.

2.decentralized training receives much less support from ML systems like
TensorFlow, MXNet and CNTK, which makes it difficult to apply this less explored
but potentially superior approach to real world problems.

**Major contribution:**

This paper proposes Hop, a heterogeneity-aware decentralized training protocol.

They start with identifying a unique characteristic of decentralized training,
the iteration gap, and determine its upper-bound based on communication graph
among workers. This property affects the cost and correctness of an
implementation. They show that one of the current designs, notify-ack, in fact
conservatively bounds the gap, but sacrifices the performance and implementation
flexibility.

They propose a queue-based synchronization mechanism for distributed
coordination. Decentralized training can be realized using update queues sized
based on the iteration gap, or using both update and token queues which can
control the iteration gap.

They propose backup workers and bounded staleness in the decentralized setting.
Importantly, they show that the queue-based synchronization is indispensable in
realizing these concepts due to fundamental reasons.

To cope with deterministic slowdown, they propose skipping iterations so that
the effect of slower workers is further mitigated.

The experiment results on CNN and SVM show significant speedup over standard
decentralized training in heterogeneous settings.
