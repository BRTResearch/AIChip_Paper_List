**Paper title:**

GOBO: Quantizing Attention-Based NLP Models for Low Latency and Energy Efficient
Inference

**Publication:**

MICRO’2020

**Problem to solve:**

BERT models are particularly expensive to train, so in typical applications we
start with a pre-trained version which we then refine to a target.

Current architecture modifications and quantization methods require fine-tuning
and often sacrifice accuracy. It is best to find model compaction methods that
can work directly off the fine-tuned models.

**Major contribution:**

GOBO accepts as input a trained BERT model and reduces the number of bits needed
to represent its parameters.

Advantages:

1.  GOBO maintains accuracy without any further model refinement such as
    retraining or fine-tuning, which requires access to the dataset which may
    not be available or may be not possible under strict time constraints.

2.  can be used as an off- and potentially on-chip compression method to reduce
    footprint, traffic and energy and thus amplify bandwidth, capacity,
    performance and energy efficiency.

3.  reduces memory traffic and energy and increases effective memory capacity.

4.  simplify computation converting most multiplications in additions.

How to do:

1.  determine outlier weights and stores the few outlier weights as-is.

2.  uses a dictionary of very few (typically 8) representative values for all
    other weights. It stores the vast majority of the weights as 3b indexes.
