**Paper title:**

DeepSniffer: A DNN Model Extraction Framework Based on Learning Architectural
Hints

**Publication:**

ASPLOS\`20

**Problem to solve:**

The adversarial attack on DNN still need further research because:

1.  Previous studies extract the model architecture information with following
    limitations: requiring a priori knowledge of victim models, lacking in
    robustness and generality, or obtaining incomplete information of the victim
    model architecture.

2.  A model information extractor robust to architectural and system noises
    introduced by the complex memory hierarchy and diverse runtime system
    optimizations is required.

**Major contribution:**

DeepSnifer: a learning-based model extraction framework to obtain the complete
model architecture information without any prior knowledge of the victim model.

It has following advantages:

1.  Only using kernel\`s execution latency, read volume, write volume, and mem
    address trace to reconstruct the DNN model and data size. The information
    above is easily to require and makes the extractor robust.

2.  Mapping the DNN layer sequence to the speech recognition problem, and using
    the CTC method to search the layer sequence.

In general, this is a DNN security paper, which is few related with computer
architecture design.
