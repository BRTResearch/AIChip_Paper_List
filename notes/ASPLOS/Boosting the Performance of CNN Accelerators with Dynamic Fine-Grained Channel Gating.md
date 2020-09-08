**Paper title:**

Boosting the Performance of CNN Accelerators with Dynamic Fine-Grained Channel
Gating

**Publication:**

ASPLOS’18

**Problem to solve:**

Convolutional neural networks (CNNs) have demonstrated human level accuracy in
many vision-related tasks and are being increasingly adopted for many
applications, including real-time tasks such as autonomous driving and robotic
manipulation. Unfortunately, state-of-the-art CNNs are highly compute-intensive,
as they typically demand about 10\^9 floating point operations (FLOPs) per
inference. In order to deploy CNNs in a much broader range of applications,
especially in embedded and mobile settings, we need to reduce the high
computational cost without noticeably sacrificing inference accuracy.

**Major contribution**

Propose a new dynamic pruning technique, named channel gating (CGNet), which
removes ineffectual computations specific to each input at run time, and present
a hardware accelerator architecture to effectively exploit the dynamic sparsity
introduced by channel gating.

Experimental results show that the proposed approach can significantly speed up
state-of-the-art networks with a marginal accuracy loss, and enable a trade-off
between performance and accuracy.

This paper shows that channel gating can be supported with a small set of
extensions to a CNN accelerator, and implements a prototype for quantized
ResNet-18 models. The accelerator shows an average speedup of 2.3× for ImageNet
when the theoretical FLOP reduction is 2.8×, indicating that the hardware can
effectively exploit the dynamic sparsity exposed by channel gating.
