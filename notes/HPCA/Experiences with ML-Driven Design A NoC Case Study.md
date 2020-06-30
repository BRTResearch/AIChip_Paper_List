**Paper title:**

Experiences with ML-Driven Design: A NoC Case Study

**Publication:**

HPCA’20

**Problem to solve:**

ML for system design still leaves much to be desired in a few areas. The first
is in hyperparameter tuning to get the RL agent to perform well. The second area
is the interpretability of neural networks. The third area in ML-aided design
methodology is in going from the neural network to a practical solution.

**Major contribution:**

This is a heuristic paper that opens up new research directions. In this paper,
they leverage machine learning (reinforcement learning in particular) to design
NoC arbiters. They hope that this work can provide guidance in how to fill the
gaps and apply ML techniques to design better systems.

The main methods are as follows: First, use a well-explained three-layer NN to
be the agent of RL. Second, determine the importance of the feature by analyzing
the average weight of the input feature connecting the middle hidden layer.
Third, design the hardware according to the importance of the feature. Fourth,
first analyze the simple scene of a simulator, get some conclusions, summarize
some methods, and then push to a real complex scene (e.g. APU simulator) for
analysis.

**Lessons learnt:**

This paper uses NoC's Arbitrator as an example, and uses RL to solve the task of
which data should be transmitted by the arbitrator on each router. By analyzing
the RL's Agent network, we can know which input features are important.
Therefore, we can use this information to design a simpler and more efficient
Arbitrator, instead of directly using RL's Agent.
