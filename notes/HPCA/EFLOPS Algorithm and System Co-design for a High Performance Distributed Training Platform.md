**Paper title:**

EFLOPS: Algorithm and System Co-design for a High Performance Distributed
Training Platform

**Publication:**

HPCA’20

**Problem to solve:**

Traditional server clusters have poor scalability for training due to the trafﬁc
congestions within the server and beyond. The intra-server trafﬁc on the I/O
fabric can result in severe congestions and skewed quality of service as
high-performance devices are competing with each other. Moreover, the trafﬁc
congestions on the Ethernet for inter-server communication could also incur
signiﬁcant performance degradation.

**Major contribution:**

1.  **BiGraph topology**: They divide the network into two parts (Upper and
    Lower), and each part is interconnected by the Clos architecture, which is
    like a two-layer Fat-tree topology Spine and Leaf switch. The computing
    server can be directly connected to the two parts of the switch; that is,
    each switch plays the role of Spine and Leaf in the Fat-tree topology, and
    the maximum number of hops is 3.

2.  **Topology-aware allreduce algorithm**: This algorithm maps the connections
    of the HD algorithm and the physical links of the BiGraph topology one by
    one to avoid link contention between them to completely solve the network
    congestion problem.

**Lessons learnt:**

Due to the technological breakthrough of deep neural networks, the technical
research around AI, such as AI algorithm models, training frameworks, and the
design of the underlying accelerator, has attracted more and more attention, and
its application has become more and more widely used. However, few people
explore from the perspective of cluster architecture. So this paper porposed a
high-performance AI cluster called EFlops. There are three key technologies: a
networked heterogeneous computing server architecture, a highly scalable network
architecture, and a high-performance communication library that cooperates with
the system architecture.
