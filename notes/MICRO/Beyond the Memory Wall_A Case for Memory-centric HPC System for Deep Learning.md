**Paper title:**

Beyond the Memory Wall: A Case for Memory-centric HPC System for Deep Learning

**Publication:**

MICRO’19

**Problem to solve**

As researchers seek to deploy deeper and larger DNN topologies however,
end-users are faced upon a memory “capacity” wall, where the limited on-device
physical memory constrains the algorithm that can be trained. Current trends
point to an urgent need for a system architectural solution that satisfies the
dual requirements of (a) fast inter-device communication for parallel training,
and (b) high performance memory virtualization over a large memory pool to
enable memory hungry DNNs to be trainable over accelerator devices.

**Major contribution**

This work first highlights the importance of device-side interconnects in
training scaled up DL algorithms, presenting a quantitative analysis on parallel
training in the context of HPC systems with multiple accelerator (GPU/TPU)
devices.

This work identifies key system-level performance bottlenecks on DC-DLA and
motivates the need for a new system architecture that balances fast
communication and user productivity in training large DNN algorithms.

Propose and evaluate a system architecture called MC-DLA that provides
transparent memory capacity expansion while also enabling fast inter-device
communication. Compared to DC-DLA designs, this paper achieves an average 2.8×
performance improvement while expanding the system-wide memory capacity exposed
to the accelerators to tens of TBs.
