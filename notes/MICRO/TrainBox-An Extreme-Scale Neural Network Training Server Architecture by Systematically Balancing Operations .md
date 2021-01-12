**Paper title:**

TrainBox: An Extreme-Scale Neural Network Training Server Architecture by
Systematically Balancing Operations

**Publication:**

MICRO’20

**Problem to solve:**

1.  With development of neural network, specialized accelerators, high-speed
    interconnects and algorithms have be proposed, so the bottleneck of neural
    network is shifted from computation and inter-accelerator communication to
    data preparation.

2.  The data augmentation can not be skipped for it is one of the important
    hyperparameters. And because of the huge requirements for memory, augmented
    data can’t be stored in device in advance.

3.  The model computation and model synchronization overlap the overhead of data
    preparation.

**Major contribution:**

Authors analyze the main consumption of lager scale neural network, and find
that the overhead of computation over system has shifted from model computation
and inter-accelerator communication to data preparation, especially data
transformation for neural network specific formats and buffering for
communication among devices. To reduce the burden of data preparation od system,
authors propose a scalable neural network server architecture.

1.  The authors enlighten the importance of data preparation for neural network
    servers at scale.

2.  Four design guidelines, which are applicable to board spectrum of neural
    network models and input types, to enable scalable neural network servers is
    proposed.

3.  A novel TrainBox architecture is proposed, which can effectively remove the
    performance bottleneck caused by the limited host-side resources, and
    achieves high scalability by efficiently utilizing scalable interconnects
    with three key optimizations.

4.  The authors’ research reveals that the heavy resource consumption comes from
    data transformation for neural network specific formats and buffering for
    communication among device
