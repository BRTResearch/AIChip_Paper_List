**Paper title:**

Towards Pervasive and User Satisfactory CNN across GPU Microarchitectures

**Publication:**

HPCA’17

**Problem to solve:**

Recently, with the increasing compute power of mobile GPUs, there is growing
interest in performing inference on mobile platforms. As a result, CNN-based
applications are becoming pervasive across all GPU platforms. However, due to
differences between GPU hardware resources, the optimal configuration of CNNs on
one GPU may not be suitable on another.

The authors try to understand the specific implementation of CNNs on GPUs and
craft an analytical model to predict the performance of CNNs among different GPU
architectures. With a platform-independent analytical model, CNN models trained
on high-end GPUs can be efficiently deployed on different platforms without
time-consuming retraining. It is important to note that the optimization goals
of these two stages (i.e., training and inference) are different. The goal of
the training stage is to obtain high accuracy as soon as possible. The inference
stage, however, is closer to the end- user and its goal varies based upon the
specific task. Real-time tasks need a small latency to perform inference, such
as real- time surveillance and autonomous driving. Background and
batch-processing tasks are not sensitive to runtime, but are more concerned
about energy consumption. Some interactive tasks are sensitive to runtime, but
can tolerate some delay. In addition to runtime and energy, CNN-based
applications have a distinctive signature: accuracy. Interestingly, high
accuracy is not always preferred in the inference stage, especially when the
accuracy of a state- of-the-art CNN can outperform human-level accuracy. For
example, some entertainment applications do not need high accuracy, such as
Moments. Lowering the accuracy can even improve user experience since the
unnoticeable accuracy decrease leads to faster response time. For some
applications in security and scientific research, higher accuracy is preferred.
Thus, the influence of accuracy on user experience is also determined by the
specific task.

The authors try to propose a framework to balance all requirement and achieve a
better user experience.

**Major contribution:**

To evaluate the user experience of the inference, the authors first investigate
the influence of runtime, power, and accuracy on user satisfaction, and then
provide a user satisfaction-of-CNN metric (i.e., SoC) by combining these three
factors.

To ensure ideal user satisfaction on all kinds of platforms, the authors propose
Pervasive CNN, a user satisfaction-aware CNN inference framework. P-CNN has two
phases: cross-platform offline compilation and run-time management. Based on the
specifications of CNN-based applications, P-CNN can infer the requirements of
end-users. Then, according to these requirements, offline compilation generates
the optimal kernel for the deployed platforms and provides scheduling
information for run-time management. The runtime management phase consists of
accuracy tuning, execution, and calibration. First, accuracy tuning dynamically
identifies the fastest kernels with acceptable accuracy. During this phase, a
series of tuning tables are generated for the following calibration. Based on
the tuning table, the run-time kernel scheduler partitions the optimal GPU
computing resource to each layer and then schedules the GPU thread blocks. As
the input data can change during run-time, P-CNN monitors the accuracy of the
output. If its accuracy is not tolerated by the end-user, calibration chooses a
less aggressive tuning table (corresponds to a slower but more precise kernel)
to improve the accuracy of output.

To ensure that the actual response time of CNN-based applications is within the
tolerance of end-users, the authors first develop a platform-independent time
model to estimate the execution time of CNNs. They then use this time model to
guide cross-platform offline compilation. To generate the optimal kernels for a
specific GPU architecture, the authors first characterize the deep learning
libraries to reveal two main tuning parameters: sub-matrix size and register
consumption per thread, which dominate the performance of the convolutional
kernel. They then design an analytical metric to select the optimal kernel by
coordinately fine-tuning these two parameters.

By comparing with multiple run-time scheduler schemes, P-CNN can obtain the best
user satisfaction for different inference tasks across various GPU platforms.
Evaluation results also show that our entropy-based approximate method achieves
the same effect (i.e. 1.8x speedup within 10% accuracy loss) as the
accuracy-based method.

**Lessons learnt:**

This work is a systemic work. The balancing of different goal is very inspiring,
and the idea of CNN requirement predicting and dynamic kernel choosing is very
promising in real world application.
