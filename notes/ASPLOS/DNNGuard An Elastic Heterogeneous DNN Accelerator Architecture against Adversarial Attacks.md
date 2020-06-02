**Paper title:**

DNNGuard: An Elastic Heterogeneous DNN Accelerator Architecture against
Adversarial Attacks

**Publication:**

ASPLOS’20

**Problem to solve:**

1.  Attackers can construct adversary samples that are able to deceive DNN
    models to make false predictions by carefully performing minor perturbation
    to the normal samples.

2.  Existing DNN accelerators cannot effectively support the defense methods
    such as machine learning denoising;

3.  Deploying the two networks in loosely coupled two accelerators will lead to
    potential information leakage.

**Major contribution:**

DNNGuard adopts a tightly-coupled heterogeneous architecture with a CPU core and
an elastic DNN accelerator to support diverse adversary sample defense methods.
Major contributions are as follows:

1.  An elastic on-chip buffer management mechanism;

2.  An elastic PE computing resource management;

3.  An extended AI instruction set.

**Lessons learnt:**

Firstly, this paper considers that two different networks need to be run in the
situation that adversary samples exist. Simply reusing DNN accelerator does not
achieve the highest efficiency. So they thought of using the CPU to do some
serial tasks to ease the pressure on the DNN accelerator, but this will bring
high latency caused by data movement. In the end, they designed a complex
storage model and corresponding data movement mechanism to effectively calculate
two neural networks simultaneously.

Secondly, the paper mentioned the information security of neural networks.
According to their theory, tightly coupling the DNN accelerator and the CPU core
in a chip can effectively protect information. However, due to the limitations
of my knowledge, I did not see why this can improve the security of information.
