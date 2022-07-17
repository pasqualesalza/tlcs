---
title: Configuration
weight: 2
katex: true
---

We produced the _Multimodal Embedding Model (MEM)_ architecture, starting from the one proposed by [_Husain et al._](https://arxiv.org/abs/1909.09436) for the [_CodeSearchNet_](https://github.com/github/CodeSearchNet) challenge.

![MEM](/mem.png?width=50pc&classes=border,shadow)

We publicly release the source code:

{{% button href="https://github.com/pasqualesalza/tlcs/raw/main/data/source/src-finetuning.tar.xz" icon="fas fa-download" %}}src-finetuning.tar.xz{{% /button %}}

## Hyperparameters

The following table shows the fine-tuning hyperparameters compared to the ones used by *Husain et al*.

Parameter | _Husain et al._ | Our approach
--- | ---: | ---:
Learning rate | 0.0005 | 0.0005
Learning rate decay | 0.98 | 0.98
Momentum | 0.85 | 0.85
Dropout probability | 0.1 | 0.1
Maximum sequence length (query) | 30 | 30
Maximum sequence length (code) | 200 | **256**
Optimizer | Adam | **LAMB**
Maximum training epochs | 500 | **10**
Patience | 5 | **10**
Batch size | 450 | **32**

Then, we report the $\text{BERT}$-specific hyperparameters that we used for both the code encoder and the query encoder.

Parameter | _Husain et al._ | Our approach
--- | ---: | ---:
Activation function | gelu | gelu
Attention heads | 8 | 8
Hidden layers | 3 | 3
Hidden size | 128 | **768**
Intermediate size | 512 | **3,072**
Vocabulary size | 10,000 | **30,522**
