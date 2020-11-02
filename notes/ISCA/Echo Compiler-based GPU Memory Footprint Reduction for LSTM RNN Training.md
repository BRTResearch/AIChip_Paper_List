**Paper title:**

Echo: Compiler-based GPU Memory Footprint Reduction for LSTM RNN Training

**Publication:**

ISCA’20

**Problem to solve:**

1. LSTM RNN tends to be less efficient on modern GPU as the high GPU memory
consumption limits the maximum training batch size.

2. Prior works that propose efficient compression techniques for inference focus
on weights rather than feature maps. Prior works for reducing DNN training
footprint is not suitable for LSTM RNNs.

3. Reducing footprint by feature map recomputation in prior works fail to
deliver satisfactory footprint reduction in the case of LSTM RNN training and
other state-of-the-art training workloads.

4. Prior works cannot accurately estimate footprint reduction and
non-conservatively estimate runtime overhead.

**Major contribution:**

They do a research on how the GPU memory is consumed and where the runtime is
spent in NMT(Neural Machine Translation) model. The result reveals that the
feature maps of the attention and RNN layers form the memory bottleneck and the
runtime is unevenly distributed across different layers.

They propose Echo, a new compiler-based optimization scheme. For accurately
estimating footprint reduction, Echo makes footprint reduction estimation
practical by partitioning the whole computation graph into smaller subgraphs to
restrict the scope (and hence reduce the complexity) of the footprint reduction
estimation. Compute-heavy layers form the natural boundaries for partition,
since they are not recomputed and therefore out of the estimation scope. Echo
then analyzes each small subgraph independently and makes accurate footprint
reduction estimation for recomputation.

To non-conservatively estimate runtime overhead, Echo infers the data
dependencies of the gradient operators. Only if the gradient computation
requires the forward operators’ outputs will the forward operators’ runtime be
added as a part of the recomputation overhead estimate.

They implement Echo by open-sourced MXNet and NNVM which is a state-of-the-art
machine learning framework graph compiler. Echo reduces the GPU memory footprint
transparently and automatically for numerous machine learning models without any
changes to the training source code.

They evaluate Echo on numerous state-of-the-art machine learning workloads,
including NMT, DeepSpeech2, Transformer, and ResNet, on real systems with modern
GPUs and observe footprint reduction ratios of 1.89x on average and 3.13x
maximum.

**Lessons learnt:**

1. Reducing footprint by recomputation needs additionally stash data in memory
for computing new feature maps and runtime overheads. Using efficient approach
to optimize these two challenges can improve more performace.

2. Footprint reduction works for CNN like Gist is not suitable for LSTM RNN as a
result of high runtime overhead for many small vector layers used in LSTM RNNs,
or limited applicability because of the difference model structure.
