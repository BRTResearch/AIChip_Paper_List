**Paper title:**

SCALEDEEP: A Scalable Compute Architecture for Learning and Evaluating Deep
Networks

**Publication:**

ISCA’2017

**Problem to solve:**

1.  DNNs impose significant computational challenges owing to the complexity of
    the networks and the amount of data they process, both of which are
    projected to grow in the future.

2.  The extreme computational challenge imposed by DNNs: (i) Embedded inference,
    in which DNNs need to be deployed and evaluated on energy-constrained
    devices such as phones, wearables and IoT edge devices, and (ii) Cloud-based
    training, in which DNNs are trained in the cloud using massive amounts of
    data, requiring very high training times.

3.  However, even state-of-the-art software implementations may take several
    days to weeks to train large-scale networks, necessitating new approaches
    for efficiency. SCALEDEEP falls into this category, but differs in two key
    ways -almost all prior efforts focus on DNN evaluation, and design
    standalone hardware IPs (cores) that realize key computational kernels
    within DNNs

**Major contribution:**

1.  We propose a high performance server architecture, called SCALEDEEP, which
    is designed from the ground-up for DNN training and evaluation. We
    specialize all subsystems of SCALEDEEP, including compute cores, memory
    hierarchy and inter-connect topology, based on the key computation and data
    access patterns in DNNs, leading to drastic improvements in performance and
    energy efficiency

2.  SCALEDEEP differs from prior efforts on DNN hardware in two key ways: (i)
    SCALEDEEP primarily targets largescale training of DNNs in contrast to most
    prior efforts, which focus on network evaluation. Training encompasses
    network evaluation as one of its steps, but presents a broader set of
    computational challenges. (ii) While most efforts propose standalone
    accelerator cores, SCALEDEEP is a scalable server architecture composed of
    thousands of such processing cores, and deals with system-level challenges
    such as improving core utilization, memory bandwidth and reducing
    synchronization overheads.

3.  Heterogeneous processing tiles and compute chips that aggressively exploit
    the diverse FLOPs and Bytes/FLOP requirements of operations within DNNs. A
    3-tiered grid-wheel-ring interconnect topology that matches the key memory
    access and communication patterns of DNNs, including convolution/matrix
    multiplication followed by feature accumulation within a layer, producer
    consumer relationship across layers, and data vs. model parallelism across
    inputs in a minibatch. A low-overhead scheme to enforce synchronized
    execution using hardware data-flow trackers. Methods to map DNNs that
    minimize data movement and improve core utilization through nested
    pipelining.

**Lessons learnt:**

The architecture of SCALEDEEP comprises of heterogeneous processing tiles with
CompHeavy tiles and MemHeavy tiles, and heterogeneous compute chips with
ConvLayer chips and FcLayer chips, interconnected using a 3-tiered
grid-wheel-ring topology. This leverages the computation and communication
patterns prevalent in DNNs.
