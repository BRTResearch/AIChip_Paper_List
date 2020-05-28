**Paper title:**

FPSA: A Full System Stack Solution for Reconfigurable ReRAM-based NN Accelerator
Architecture

**Publication:**

ASPLOS’19

**Problem to solve:**

1，communication bottleneck between PE

2，peripheral circuits overhead(computation bound)

3，every layer‘s computation and storage balance

This paper points out that the technology of PEs based on RRAM crossbar to solve
the problem of "memory wall" in NN accelerators has been widely studied.
However, the high efficiency and high density advantage of RRAM have not been
fully utilized due to the huge communication demand between PEs and the high
overhead of peripheral circuits.

This paper proposes a full system stack solution, composed of a reconfigurable
architecture design, Field Programmable Synapse Array (FPSA) and its software
system including neural synthesizer, temporal-to-spatial mapper, and placement &
routing. To satisfy the high-performance communication demand, the paper
optimizes it with a reconfigurable routing architecture and the placement &
routing tool mrFPGA. To improve the computational density, it simplifies the PE
circuit with the spiking schema and highly leverages software to use hardware
resources efficiently, rather than complicating hardware.

Evaluations show that, compared to PRIME, the computational density of FPSA
improves by 31x ; for its inference performance can achieve up to 1000x speedup.

**Major contribution:**

-   This paper proposes a full stack solution for ReRAM-based NN accelerator,
    including a reconfigurable architecture, FPSA, and the software hierarchy.
    The latter fully utilizes the various kinds of programmable resources
    provided by the former to deploy NN efficiently. The software includes the
    allocation of hardware resources at each layer, and how to map DFG to PE
    hardware units.

-   This paper claims that communication latency is the bottleneck of existing
    ReRAM-based NN accelerator and then propose to optimize it with the FPGA's
    reconfigurable routing architecture instead of the memory bus and NOC to
    break this bound. And the switch boxes and connection boxes are both
    RRAM-based cells. (mrVPA is used for layout and wiring which is proposed in
    mrFPGA).

-   The paper reduces the area of a single PE with using spiking schema to push
    the performance to the high-utilization region of the utilization bound for
    a given chip area and propose an add method that will add the conductance
    values evenly to increase precision and reduce RRAM variation.

**Lessons learnt:**

RRAM-based NN accelerator has been mainly focused on the calculation unit in the
past studies. This study attempts to optimize the communication mode of NN
accelerator by introducing FPGA reconfigurable routing and further using RRAM
cell to further reduce the routing area.
