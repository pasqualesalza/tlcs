---
title: Configuration
weight: 2
katex: true
---

We customized the original $\text{BERT}_\text{base}$ configuration by _Google_, whose source code can be found at https://github.com/google-research/bert, to deal with the context of source code as input.

We publicly release the source code:

{{% button href="https://github.com/pasqualesalza/tlcs/raw/main/data/source/src-pretraining.tar.xz" icon="fas fa-download" %}}src-pretraining.tar.xz{{% /button %}}

## Hyperparameters

Thus, we produced a $\text{BERT}_\text{custom}$ configuration.

The following table shows the pre-training hyperparameters compared to $\text{BERT}_\text{base}$.

Parameter | $\text{BERT}_\text{base}$ | $\text{BERT}_\text{custom}$
--- | ---: | ---:
Optimizer |  Adam | Adam
Learning rate | 0.0001 | 0.0001
$\beta_1$ | 0.9 | 0.9
$\beta_2$ | 0.999 | 0.999
L2 weight decay | 0.01 | 0.01
Learning rate decay | linear | linear
Dropout probability | 0.1 | 0.1
Activation function | gelu | gelu
Masking rate | 0.15 | 0.15
Hidden size | 768 | 768
Intermediate size | 3,072 | 3,072
Attention heads | 12 | 12
Hidden layers | 12 | 12
Vocabulary size | 30,522 | 30,522
Maximum sequence length | 512 | **256**
Batch size | 256 | **62**
Learning rate warmup steps | 10,000 | **1,000**
