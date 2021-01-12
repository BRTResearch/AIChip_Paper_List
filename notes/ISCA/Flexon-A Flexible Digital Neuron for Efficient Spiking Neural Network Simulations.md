**Paper title:**

Flexon-A Flexible Digital Neuron for Efficient Spiking Neural Network
Simulations

**Publication:**

ISCA’18

**Problem to solve:**

1.  To support any neuron models, some frameworks rely on general-purpose
    processors at the cost of inefficiency in simulation speed and energy
    consumption. And the other frameworks employed specialized accelerators to
    overcome the inefficiency can only support limited set of neuron models.

2.  No matter CPU- or GPU-based SNN simulations greatly suffer from the neuron
    computation phase. Throughout the SNNs employing different differential
    equation solvers and running on different general-purpose hardware, neuron
    computation incurs a considerable amount of latency.

3.  There exist redundant hardware units, for example all of per-feature data
    paths excluding the one for AR utilize multiplication units, and the
    multiplication units redundantly exist across the data paths.

**Major contribution:**

The previous models used to simulate the SNNs are either inefficiency or limited
for all set of neuron models. So the authors design and propose a flexible
digital neuron which simulate most kind of neuron states, and improve it to save
chip area.

1.  By analyzing diverse neuron models, it can be fond that the neuron models
    share a set of biologically common features. The features can be grouped
    together to form a complete neuron model such as LIF model, and different
    combinations of the features can be used to express different neuron models
    as LLIF model.

2.  Using data paths implementing the biologically common features, Flexon which
    can achieves high flexibility by being able to simulate diverse neuron
    models is proposed.

3.  The folded Flexon can further reduce the required chip area by eliminating
    the redundant arithmetic units in the baseline Flexon.
