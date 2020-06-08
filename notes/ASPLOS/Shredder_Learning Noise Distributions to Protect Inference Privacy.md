**Paper title:**

Shredder: Learning Noise Distributions to Protect Inference Privacy

**Publication:**

ASPLOS’20

**Problem to solve:**

A wide variety of deep neural applications increasingly rely on the cloud to
perform their compute-heavy inference. This common practice requires sending
private and privileged data over the network to remote servers. Nevertheless,
the systems and computational infrastructure in use seem to have been designed
for offering functionality without foundational consideration for privacy. Such
a gap is more concerning today since cloud-based deep learning service make
their way to the households as home automation devices or shape our social,
political, and economical interactions.

**Major contribution:**

To address above problem, this paper devises Shredder, an end-to-end framework,
that, without altering the topology or the weights of a pre-trained network,
learns additive noise distributions that significantly reduce the information
content of communicated data while maintaining the inference accuracy. To find
the suitable noise distributions, Shredder adopts a disjoint offline learning
process with a loss function that strikes a balance between information loss and
accuracy loss. The central idea of learning the noise distributions enables
Shredder to mathematically incorporate accuracy as well as the measure of
privacy, and if available, the information that is expected to remain private in
the loss function. This loss function exposes a knob for asymmetrically trading
off a modest loss in accuracy for significant improvement in privacy. As such,
Shredder can use the conventional stochastic gradient descent–used for training
machine learning algorithms–to learn the noise distributions.

**Lessons learnt:**

In the future, pay close attention to human rights, privacy and trust issues in
machine learning.
