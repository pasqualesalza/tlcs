---
title: 'Homepage'
katex: true
---

# On the Effectiveness of Transfer Learning for Code Search

## Replication package

This documentation website refers to the replication package for the paper:
> **On the Effectiveness of Transfer Learning for Code Search**
> 
> The Transformer architecture and transfer learning have marked a quantum leap in natural language processing, improving the state of the art across a range of text-based tasks. This paper examines how these advancements can be applied to and improve code search. To this end, we pre-train a BERT-based model on combinations of natural language and source code data and fine-tune it on pairs of StackOverflow question titles and code answers. Our results show that the pre-trained models consistently outperform the models that were not pre-trained. In cases where the model was pre-trained on natural language "and" source code data, it also outperforms an information retrieval baseline based on Lucene. Also, we demonstrated that the combined use of an information retrieval-based approach followed by a Transformer leads to the best results overall, especially when searching into a large search pool. Transfer learning is particularly effective when much pre-training data is available and fine-tuning data is limited. We demonstrate that natural language processing models based on the Transformer architecture can be directly applied to source code analysis tasks, such as code search. With the development of Transformer models designed more specifically for dealing with source code data, we believe the results of source code analysis tasks can be further improved.

The paper is published in the journal *IEEE Transactions on Software Engineering (TSE)*.

In our work, we design a **Multimodal Embedding Model (MEM)** architecture, which leverages the predictive capabilities of [$\text{BERT}$](https://github.com/google-research/bert), a state-of-the-art, _Transformer_-based _NLP_ model, and makes use of **transfer learning** to improve the performance on code search.

![MEM](mem.png?width=50pc&classes=border,shadow)

We evaluate the performance of our models using the _StackOverflow_ dataset that we specifically mined for this purpose.

The main contributions of our work are:

* the application of _Transformers_ and _transfer learning_ to code search and evaluation
* the design of custom pre-training tasks for source code modeling and making the pre-trained source code models available to the research community
* a combined approach based on the pre-filtering of search candidates by _Lucene_ and then refined by a _MEM_
* the mining and publishing of a code search evaluation dataset from _StackOverflow_

In the rest of the pages, we provide all the data and scripts we used in our study.

## <i class="fas fa-sitemap"></i> Organization

* [Pre-training](pretraining)
  * [Data](pretraining/data) – the description and reference to the data we collected to pre-train the $\text{BERT}$ models
  * [Configuration](pretraining/configuration) – the configuration we used to pre-train the models
  * [Models](pretraining/models) – the pre-trained $\text{BERT}$ models, ready to be loaded and used for other tasks, or to replicate the rest of our study
* [Fine-tuning](finetuning)
  * [Data](finetuning/data) – the _StackOverflow_ data description and files we collected to fine-tune our _MEM_ architecture
  * [Configuration](finetuning/configuration) – the configuration we used to fine-tune the models
* [Evaluation](evaluation)
  * [Experiments](evaluation/experiments) – the description of all the experiments we performed in our study
  * [Results](evaluation/results) – the results data we collected
  * [Analysis](evaluation/analysis) – the full analysis we performed, in form of a _Python Jupyter Notebook_

## <i class="fas fa-copyright"></i> License

This replication package is licensed under the terms of the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
Please see the [license page](license) for full details.

## <i class="fas fa-user-friends"></i> Credits

* [Pasquale Salza](mailto:salza@ifi.uzh.ch) - University of Zurich, Switzerland
* [Christoph Schwizer](mailto:christoph@schwizer.dev) - University of Zurich, Switzerland
* [Jian Gu](mailto:gu@ifi.uzh.ch) - University of Zurich, Switzerland
* [Harald C. Gall](mailto:gall@ifi.uzh.ch) - University of Zurich, Switzerland
