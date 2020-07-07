**Paper title:**

FlexFlow: A Flexible Dataflow Accelerator Architecture for Convolutional Neural
Networks

**Publication:**

HPCA’17

**Problem to solve:**

CNNs computing have three types of parallelism: Feature map Parallelism(FP,
multiple output feature maps and input feature maps are processed at a time),
Neuron Parallelism(NP, multiple neurons of one output feature map are processed)
and Synapse Parallelism(SP, multiple synapse of one kernel are processed)

Most of state-of-art CNN accelerator support a specific type of parallelism, so
that the achievable performance may less than the nominal value in a specific
CNN model.

**Major contribution:**

They propose a hardware architecture that can hold above three parallelism and
combine multiple types of parallelism to improve the computing resource
utilization.

To support more types of parallelism, they remove the interface for exchanging
operands with neighbor PEs instead of adders within each PE row for adder tree.
PEs get operands through vertical and horizontal Common Data Bus (CDB). Each PE
has two buffers to store input feature map and kernel. Thus, each row of PE can
support three types of parallelism.

They propose multiple strategies to optimize the dataflow from on-chip buffers
to PEs.

From on-chip buffer to distribution layer (a layer distribute data to PE), two
strategies are used. In-Advanced Data Placement (IADP) is to arrange data for
each on-chip buffer in advance according to the logical grouping of PEs. Kernel
data, input feature map layout and output map layout should be formed. In-Place
Data Replication (IPDR) means that data in reading controller is replicated many
times to fed all PEs within one group through buses.

From distribution layer to local buffers of PEs, two strategies are used. Relax
Alignment(RA) is to exploit data overlap between adjacent location of input
neurons. The neurons can be assigned to the two PE rows in alignment way by RA.
Relax Synchronization (RS) pre-load the data in a PE and the PEs located in the
same column that use the same data later.

From local buffer to operator, they use Finite State Machine to control
dataflow.

Additionally, they implement a practical accelerator in 65nm process, and make
comprehensive evaluations from computing resource utilization, performance,
power, energy, and scalability
