**Paper title:**

ConfuciuX: Autonomous Hardware Resource Assignment for DNN Accelerators using
Reinforcement Learning

**Publication:**

MICRO’20

**Problem to solve:**

DNN is being deployed into many real-time applications. The architecture of DNN
accelerators is determined by two key components: dataflow style and total HW
resources. A lot of previous research has focused on designing efficient
dataflow strategies to extract reuse. But the assignment of HW resources is the
crucial part. In this paper, they try to find a system that can find optimal HW
resource assignments.

**Major contribution:**

In this paper, a system called ConfuciuX is introduces which can efficiently
search through the HW design-space given a target model, platform constraints,
deployment scenario and optimization objective and determines an optimized HW
assignment strategy. Results show that the accelerator architecture generated
has better performance than traditional architectures.

The two important component in ConfuciuX is the RL Agent and the Policy Network
Architecture.

RL agent includes an actor that formulates the policy for taking actions and a
critic which approximates the value function that predicts expected reward to
help the training of policy. The author writes that they choose REINFORCE as
their RL algorithm which shows a best performance in their experiments.

The policy network is a neural network used to learn the policy to maximize the
probability of receiving better reward. The author mentioned that they use an
RNN with one LSTM hidden layer as the policy network after evaluating between
RNN and MLP.
