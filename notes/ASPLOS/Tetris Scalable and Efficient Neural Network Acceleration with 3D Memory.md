**Paper title:**

Tetris: Scalable and Efficient Neural Network Acceleration with 3D Memory

**Publication:**

ASPLOS’17

**Problem to solve:**

Scaling NN accelerators for higher performance with increasingly larger NNs
exacerbates the cost and energy overheads of their memory systems, including the
on on-chip SRAM buffers and the off-chip DRAM channels.

**Major Contributions:**

This paper presents the hardware architecture and software scheduling and
partitioning techniques for TETRIS, a scalable NN accelerator using 3D memory.

1.  Move portions of the NN computations close to the DRAM banks to decrease
    bandwidth pressure and increase performance and energy efficiency.

2.  Present an analytical scheduling scheme that matches the efficiency of
    schedules derived through exhaustive search.

3.  Develop a hybrid partitioning scheme that parallelizes the NN computations
    over multiple accelerators.

4.  Carry on experiments to show that TETRIS improves the performance by 4.1x
    and reduces the energy by 1.5x over NN accelerators with conventional,
    low-power DRAM memory systems.
