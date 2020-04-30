Master of None Acceleration: A Comparison of Accelerator Architectures for
Analytical Query Processing

Corresponding author

Andrea Lottarini, Google, PhD at Columbia University

Martha A. Kim, Columbia University

Keywords

Analytical query processing hardware, programmable homogeneous architecture,
database accelerator, RTL implementation

Summary

*Challenge*

Hardware accelerators architecture design and comparison for analytical query
processing.

数据库应用硬件加速器的架构方向选择，专用异构还是通用多核？

*Contribution*

1.  Propose a homogeneous systolic array architecture for analytical query
    processing

2.  Develop an RTL implementation for this architecture

3.  Compare a previously proposed heterogeneous hardware accelerator for
    analytical query processing to the homogeneous systolic array alternative.
    Analysis the result.

*Result*

We find that the heterogeneous and homogeneous accelerators are **equivalent for
large designs**, while **for small designs the homogeneous is better**. Our
analysis explains this counter-intuitive result, finding that the homogeneous
architecture has higher average resource utilization and lower relative costs
for the communication infrastructure.
