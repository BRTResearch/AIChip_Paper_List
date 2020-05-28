**Paper title:**

MaxNVM: Maximizing DNN Storage Density and Inference Efficiency with Sparse
Encoding and Error Mitigation

**Publication:**

MICRO’19

**Problems to Solve:**

For state-of-the-art DNN hardware accelerators, fetching weights from DRAM is a
main performance and energy bottleneck, limiting inference efficiency. Ideally,
DNNs weights would be stored entirely on-chip. However, even with aggressive
weight compression, the capacity requirements are unrealistic for storage in
on-chip SRAM.

Emerging embedded non-volatile memory (eNVM) technologies are one promising
solution for eliminating DRAM inefficiencies. Compared to SRAM, eNVMs provide
high-capacity, low read-latency storage and can be significantly denser than
SRAM. More importantly, eNVMs have multi-level cell (MLC) capabilities. With
these superior characteristics, it is promising to put all weight parameters
on-chip and hence eliminate data transfer from/to off-chip memory which cause
significant performance and energy inefficiency.

**Major Contributions:**

Generally, DNN weights are sparse. Employing lossless sparse encodings to reduce
required storage would be strictly beneficial for traditional memory
technologies like SRAM. If MLC capabilities of eNVMs can be fully employed and
combined with existed sparse encoding technologies, then it is promising to fit
all weights on-chip. However, real eNVM device is not ideal, inter-level fault
often occurs due to intrinsic randomness of physical mechanism. Unfortunately,
data structures of sparse encoding are vulnerable to inter-level faults of MLC.
Simply combine both technologies will cause significant accuracy loss. This
paper mainly solve this incompatibility and the major contributions can be
summarized as follows:

-   This paper considers fault-prone MLC eNVMs and sparse encoded weights. Under
    the restriction of not reducing accuracy, the paper studies the
    vulnerability of sparse encoding to MLC inter-level faults and determines
    the highest configuration of number of bits per cell. Results show that MLC
    capability cannot be fully employed, that is, number of bits per cell cannot
    be set as the maximum in order to avoid significant accuracy loss.

-   To further increase storage density, this paper improves DNN fault tolerance
    using protective logic. Index Synchronization, a proposed fault mitigation
    technique, and ECC are considered. With judicious use, the total number of
    required memory cells to store DNN weights decreases by up to 22% with
    proposed technique, and ECC overhead is never more than 1% of total DNN
    storage. Optimal MLC designs provide up to 29× area reduction relative to
    SLC eNVM.

-   To fit weight parameters on-chip, many techniques, such as sparse encoding,
    MLC, ECC, are used, which result in a large design space. This paper
    presents a principled co-design method to consider algorithm-to-circuit
    effects and maximize benefit. When proposing this new memory system with
    co-design approach for NVDLA, weights for state-of-the-art CNNs can fit
    on-chip, eliminating the need for DRAM. Compared to the baseline NVDLA
    implementation, MLC eNVMs enable up to 3.5× lower energy per inference and
    3.2× lower power, enabling entirely on-chip ResNet50 inference in about
    2mm2.
