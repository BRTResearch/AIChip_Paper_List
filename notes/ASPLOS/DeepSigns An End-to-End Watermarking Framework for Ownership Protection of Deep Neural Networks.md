**Paper title:**

DeepSigns: An End-to-End Watermarking Framework for Ownership Protection of Deep
Neural Networks

**Publication:**

ASPLOS’19

**Problem to solve:**

The DNN is typically considered to be the intellectual property of the model
designer, as training a highly accurate DNN requires: (i) having access to a
massive collection of mostly proprietary labeled data; and (ii) allocating
substantial computing resources to fine-tune the underlying model topology
(i.e., type and number of hidden layers), hyper-parameters (i.e., learning rate,
batch size, etc.), and weights. DNN protection against Intellectual Property
(IP) infringement is particularly important to preserve the competitive
advantage of the owner and ensure the receipt of continuous query requests by
clients if the model is deployed in the cloud as a service. Embedding digital
watermarks into DNNs is a key enabler for reliable technology transfer.

The N-bits watermarking approach for embedding the IP information in the static
content (i.e., weight matrices) of DL models is proposed but posing (at least)
two limitations: (i) It incurs a bounded watermarking capacity due to the use of
the static content of DNNs (weights) as opposed to using dynamic content
(activations). Using activations (instead of weights) provides more flexibility
for watermarking. (ii) It is not robust against attacks such as watermark
overwriting by a malicious third-party. As such, the original embedded watermark
can be removed by an adversary that is aware of the watermarking method used by
the model owner.

More recent studies proposed 1-bit watermarking methodologies for DL models
built upon model boundary modification and the use of random adversarial samples
that lie near decision boundaries. Adversarial samples are known to be
statistically unstable and transferable between different models. Therefore,
even though the proposed approaches yield a high watermark detection rate (true
positive rate), they are also too sensitive to hyper-parameter tuning and
usually lead to a high false alarm rate. Note that false ownership proofs
jeopardize the integrity of the proposed watermarking methodology and render the
use of watermarks for IP protection ineffective.

The paper aims to coherent integration of robust digital watermarks into DNNs.

**Major contribution:**

This paper proposes DeepSigns, the first efficient resource management framework
that empowers coherent integration of robust digital watermarks into DNNs.
DeepSigns inserts the watermark information in the host DNN and outputs a
protected, functionality-preserved model to prevent the adversary from pirating
the ownership of the model.

DeepSigns consists of two main phases: watermark embedding and watermark
extraction. Details can be found in the paper.

**Lessons learnt:**

The paper focuses on protection of DNNs and proposes a novel algorithm for
watermark embedding and extracting. The main idea of embedding watermark in
rarely used regions of DNN activation spaces (according to training dataset) is
inspiring.
