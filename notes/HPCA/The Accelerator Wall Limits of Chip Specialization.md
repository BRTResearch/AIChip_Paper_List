**Paper title:**

The Accelerator Wall: Limits of Chip Specialization

**Publication:**

HPCA’19

**Problem to solve:**

The demise of Moor’s Law and CMOS scaling have imposed heavy pressure on the
improvement of chip development. To alleviate the gap amid the ever-growing
computational demands and the stall transistor budgets, designers and engineers
of chip turn into the chip specialization, bypassing the scaling means. However,
unextendible number of transistors using in a chip inevitably limit improving
the optimization space, yielding diminishing specialization returns, finally
running into a bound – accelerator wall. This paper primely contributed to the
question of what are the limits of future accelerators and chip specialization.

**Major contribution:**

This paper use CMOS scaling equations and datasheets from thousands of chips to
construct an application-independent CMOS potential model of a chip and use this
model to decouple the contributions of CMOS technology and specialization to
accelerator gain.

This paper develop the metric of Chip Specialization Return(CSR) and examine
popular applications and different accelerator platforms to quantify how CSR has
changed in accordance to the improvement in accelerator gains.

This paper identified commonly used chip specialization techniques and their
theoretical limitations, as well as building a modeling framework to tease apart
the gain from specialization techniques and CMOS scaling, on a range of
accelerator benchmarks.

**Lessons learnt:**

The roadmap of technique progressing may have its own principles, obviously like
Moor’s Law, Dennard scaling and etc.. Unfortunately, the history of technology
does not hold for these rules all the time, with the bound coming to break them
through and make them no sense. Meanwhile, every road leads to Rome. New one
will help to benefit in forward way. The key to find these novel way is to
carefully analyze the pros and cons of old technique, and its environments to
summarize diverse insight.
