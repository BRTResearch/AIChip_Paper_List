**Paper title:**

The dark side of DNN pruning

**Publication:**

ISCA’18

**Problem to solve:**

1.  DNN pruning may not accelerate but increase decoding time in Automatic
    Speech Recognition(ASR) system. An ASR system consists of a DNN for
    computing acoustic scores, followed by a Viterbi beam search to find the
    most likely sequence of words.

2.  Although DNN pruning accelerate the recognition of DNN, searching time in
    Viterbi part is increased, which may even slow the whole system time. When
    DNN is pruned 90%, the Viterbi search suffers a slowdown of 4.5× and the
    execution time of the ASR system is increased 33%.

**Major contribution:**

This paper showed that DNN pruning make probability distribution of output class
more disperse and decrease the probablilty of the top-1 class. The input of the
Viterbi search is the output class of the result of DNN recognition with its
probablity. DNN pruning increase the number of the input of Viterbi search.

The key idea in the paper is to constrain the Viterbi search to the N-best
hypotheses, i.e. the N paths with the smallest cost, on every frame of speech.
Therefore, only up to N hypotheses have to be stored per frame, independent to
the confidence of the DNN scores. They also introduce a novel design to loosely
select N-best hypotheses by using a K-way set-associative hash table. Their
system keeps the K paths with the smallest cost and discards the rest. In this
way, the method avoids hypotheses being put into Overflow Buffer.

The authors write two simulators that model the baseline Viterbi accelerator and
the DNN accelerator for pruned DNNs. Furthermore, they implemented the new hash
table in the Viterbi simulator. In the 90% DNN pruning, the novel method
achieves 9x energy savings and 4.2x speedup with respect to the state-of-the-art
ASR solutions.

**Lessons learnt:**

In ASR system, the pruning of DNN effect the calculation speed of Viterbi
search. The acceleration method of DNN computation may slowdown the whole
system.
