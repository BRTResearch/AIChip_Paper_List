**Paper title:**

TABLA: A Unified Template-based Framework for Accelerating Statistical Machine
Learning

**Publication:**

HPCA’16

**Problem to solve:**

Machine learning algorithms include compute-intensive workloads that can benefit
significantly from acceleration. FPGAs are an attractive platform for
accelerating these important applications. However, FPGA design still requires
relatively long design cycles and extensive expertise in hardware design.

**Major contribution:**

To tackle above challenge, the paper proposes TABLA that aims to bridge the gap
between the machine learning algorithms and the FPGA accelerators. Instead of
designing an accelerator for machine learning algorithms, TABLA generates
accelerators for a class of machine learning algorithms. The key is to identify
the commonalities across a wide range of machine learning algorithms and utilize
this commonality to provide a high-level abstraction for programmers. TABLA
provides a template-based framework to automatically generate the hardware block
which implements the gradient of the objective function. Therefore, with TABLA,
the developer only needs to specify the learning model as the gradient of the
particular objective function. The gradient function can be implemented with
less than 50 lines of code for logistic regression, support vector machines,
recommender systems, backpropagation and linear regression. TABLA automatically
generates a concrete accelerator (synthesizable Verilog code) for the specific
learning algorithm while considering high-level design parameters of the target
FPGA.

**Lessons learnt:**

The paper leveraged the insight that many learning algorithms can be expressed
as stochastic optimization problems. That is, the learning task becomes solving
an optimization problem using stochastic gradient descent that iterates over the
training data and minimizes an objective function. Although the stochastic
gradient descent solver is mostly fixed across different learning algorithms,
the objective function varies. Therefore, the accelerator for these learning
tasks can be implemented as a template design, uniform across a set of machine
learning algorithms. This template design comprises the general framework for
the stochastic gradient descent optimization.
