**Paper title:**

MLPerf Inference Benchmark

**Publication:**

ISCA’20

**Problem to solve:**

1.  There are over 100 organizations building ML inference chips, and these
    chips vary three orders of magnitude in power consumption, five orders of
    magnitude in performance.

2.  These chips are used in different situations like embedded devices,
    data-center, and their software frameworks and libraries are different.

3.  As a result, assessing ML-system performance in an architecture-neutral
    representative, and reproducible manner is a challenge.

**Major contribution:**

This paper presents a benchmarking method for evaluating ML inference systems,
containing following advantages:

1.  Representative workloads for reproducibility and accessibility.

2.  Realistic evaluation is performed with consideration of scenarios.

3.  Target qualities and tail-latency bounds are prescribed in accordance with
    real-world use cases.

4.  Benchmarking users are allowed to show both hardware and software
    capabilities with some preset permissive rules.

5.  The models in the benchmarking are allowed to change frequently while they
    can still keep aforementioned features.

**Lessons learnt:**

It’s very interesting to see such a thoroughly understanding about
NN-accelerators, datasets and benchmarking.
