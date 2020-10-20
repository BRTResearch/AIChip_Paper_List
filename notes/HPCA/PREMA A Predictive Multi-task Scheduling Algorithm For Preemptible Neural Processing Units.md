**Paper title:**

PREMA: A Predictive Multi-task Scheduling Algorithm For Preemptible Neural
Processing Units

**Publication:**

HPCA’2020

**Problem to solve:**

The key objective of this paper is twofold: 1) development of efficient
preemption mechanisms tailored for multi-tasked NPU inference, and 2) a
multi-task scheduling policy that effectively utilizes the preemptible NPU.

**Major contribution:**

1.  To the best of our knowledge, our work is the first to explore multi-tasked
    DNNs, an important and emerging problem space that has not been addressed by
    prior work.

2.  This paper is the first to provide an in-depth, quantitative analysis on the
    architectural support required for enabling preemption on NPUs.

3.  We propose PREMA, which utilizes preemption and the ability to estimate
    inference time to intelligently balance latency, throughput, and SLA
    satisfaction for multi-tasked DNNs.

**Lessons learnt:**

This paper is mainly about the model inference and scheduling in NPU, and there
has been little performance and delay research on the NPU. This paper makes a
case for a “preemptible” neural processing unit (NPU) and a “predictive”
multi-task scheduler to meet the latency demands of high priority inference
while maintaining high throughput. We evaluate both the mechanisms that enable
NPUs to be preemptible and the policies that utilize them to meet scheduling
objectives.
