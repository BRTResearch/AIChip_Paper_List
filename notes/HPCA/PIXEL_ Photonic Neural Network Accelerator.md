**Paper title:**

PIXEL: Photonic Neural Network Accelerator

**Publication:**

HPCA\`20

**Problem to solve:**

Real life applications require CNNs with millions of MAC operations in each
layer, composing several hidden layers, which poses a serious challenge for
future scaling of ANNs in general. Moreover, electronic-based accelerators
utilize broadcast and multicast buses for achieving parallelism and are still
limited by electronic clock rates and ohmic losses. This paper tries to use some
new material to replace the electronic based CNN accelerators.

**Major contribution:**

1.  Optical MAC: Two accelerators that implement efficient optical MAC
    functionality for DNNs using MRRs and MZIs. There are an electrical-optical
    hybrid version and an all-optical version of the proposed accelerator.

2.  PIXEL: PIXEL provides a scalable platform to implement CNN architectures of
    various sizes while minimizing energy-delay product (EDP) for varying number
    of wavelengths and bits/wavelength.

**Lessons learnt:**

Though the progress in energy saving by OMAC reaches an extremely high position,
the shortcomings of this kind of system is never mentioned in this paper.
