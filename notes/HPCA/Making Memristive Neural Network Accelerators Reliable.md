**Paper title:**

Making Memristive Neural Network Accelerators Reliable

**Publication:**

HPCA‘18

**Problem to solve:**

Detecting and correcting the errors that occur during in-memory analog
computation remains largely unexplored. The same electrical properties that
provide the performance and energy improvements make these systems especially
susceptible to errors, which can severely hurt the accuracy of the neural
network accelerators. Even if no one cell is in error such that it would be read
improperly in a traditional memory array, the sum of the errors when computing a
dot product operation that spans an entire row can produce incorrect results.

**Major Contributions:**

1.  The paper presents the first work on error correction schemes for memristive
    accelerators. They propose an error correction schemes based on AN codes
    that can correct the errors that occur during computation.

2.  Present a new form of data-aware AN codes that increase the error correction
    capacity by leveraging the properties of the resistive networks, and the
    importance of the error to overall system accuracy within a DNN computation.
