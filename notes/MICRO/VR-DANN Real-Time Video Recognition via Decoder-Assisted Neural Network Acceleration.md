**Paper title:**

VR-DANN Real-Time Video Recognition via Decoder-Assisted Neural Network
Acceleration

**Publication:**

MICRO‘20

**Problem to solve:**

1.  Traditional methods on video recognition feed every frame to the large
    neural network, which is time-consuming and energy consuming.

2.  Previous optimizations ignore the information from video compression
    process.

**Major contributions:**

1.  Proposed an algorithm combing with the decoder. With the information from
    motion vectors, only I-frames and P-frames are fed to the large neural
    network, and B-frames are reconstructed from I-frames and P-frames.

2.  Proposed a small neural network to refine the reconstruction result and
    remove the noise.

3.  Proposed an architecture to efficiently enable this algorithm. Proposed
    VR-DANN Agent Unit to make the kernel switching efficiently.

**Lessons learnt:**

Intrinsic information from the decoder can help to accelerate the neural
network. With the help of motion vector, the results can be reconstructed, so
that the number of frames fed to large neural network is reduced, which save
much time and energy. This paper is the first attempt to closely link video
compression process and neural network, which is attractive for this paper.
