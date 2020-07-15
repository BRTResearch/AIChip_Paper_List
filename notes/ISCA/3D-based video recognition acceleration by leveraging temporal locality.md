**Paper title:**

3D-based video recognition acceleration by leveraging temporal locality

**Publication:**

ISCA’19

**Problem to solve:**

1.  Video-based 3D-CNN has a high computational cost as its parameters are far
    more than 2D-CNN. It needs to capture spatial-temporal context across
    frames.

2.  The two points mentioned above make it infeasible to directly apply 2D-CNN
    accelerator to 3D-CNN, which includes following challenges:

    1.  Working set size of 3D-CNN exceeds on-chip memory;

    2.  3D-CNN is much more computation-intensive than memory-intensive based on
        the Roofline model;

    3.  3D-CNN exhibits more reuse opportunities: it also has temporal
        dimensional data reuse besides spatial reuse.

3.  How can accelerator use the redundancy of data to further accelerate 3D-CNN.

**Major contribution:**

1.  A thorough investigation on 3D-CNN, which shows that large data overlap
    exists between input feature maps across the temporal dimension, and
    quantization of input feature maps could increase the overlap.

2.  Propose an architecture that leverage the data overlap across the temporal
    dimension and process the computation of effectual items for 3D CNN
    efficiently (this method is called differential convolution). Then to
    further leverage both the spatial locality and temporal locality that makes
    the architecture general to all CNNs, a dynamic control mechanism to switch
    between spatial delta dataflow and temporal delta dataflow dynamically is
    proposed.
