**Paper title:**

ADMM-NN: An Algorithm-Hardware Co-Design Framework of DNNs Using Alternating
Direction Methods of Multipliers

**Publication:**

ASPLOS’19

**Problem to solve:**

1.  A systematic framework of joint weight pruning and quantization of DNNs is
    lacking. This paper tries to answer how to combine these two methods
    reasonably.

2.  The computation reduction, energy efficiency improvement, and hardware
    performance overhead caused by model compression are not thoroughly
    investigated.

**Major contribution:**

1.  An ADMM-based weight pruning and weight quantization algorithm for DNNs;

2.  A systematic, joint framework for DNN model compression;

3.  The hardware’s performance effected by pruning on Conv layers is thoroughly
    investigated.

4.  Hardware-aware DNN model compression for computation reduction and
    efficiency improvement.

**Lessons learnt:**

This paper is mainly discussing the DNN compression algorithm, but the
attractive points of this paper is the hardware part. This paper thoroughly
investigated the effect of pruning on the performance degradation on hardware,
and using that as the foundation of the hardware-adapt compression algorithm.
