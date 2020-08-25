**Paper title:**

Kelp: QoS for Accelerated Machine Learning Systems

**Publication:**

HPCA’19

**Problem to solve:**

Machine learning applications often depend on the host system. As a result,
contention on host resources, such as memory bandwidth, can significantly
discount the performance and efficiency gains of accelerators. It conducts
experiments which show that the given workloads are sensitive to host memory
bandwidth contention, which can cause 40% average performance degradation when
left unmanaged.

**Major contribution:**

1.  This paper conducts a thorough performance study of various ML workloads
    that leverage different accelerated platforms. Through a detailed
    sensitivity study, it shows that performance of these workloads can be
    significantly impacted by host memory bandwidth pressure, and demonstrate
    the need for performance isolation mechanisms.

2.  This paper explores the capabilities of existing CPU architectures to
    improve the efficiency of performance isolation. It shows that by carefully
    managing memory saturation and avoiding global throttling, this mechanism
    enables higher system efficiency compared to previous work.

3.  This paper presents Kelp, a light weight runtime system that leverages
    existing hardware features to mitigate performance interference between CPU
    and accelerated ML tasks.

4.  It shows that high-performance accelerators pose new system architecture
    challenges. Experiment results motivate CPU designers to rethink the
    implication of existing micro-architectural features and designs, and
    motivate the need for fast and low-overhead fine-grained memory performance
    isolation mechanisms.

It evaluates Kelp with both production and artificial aggressor workloads, and
compare its effectiveness with previously proposed solutions. The evaluation
shows that Kelp is effective in mitigating performance degradation of the
accelerated tasks, and improves performance by 24% on average. Compared to
previous work, Kelp reduces performance degradation of ML tasks by 7% and
improves system efficiency by 17%.
