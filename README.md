# On the Effectiveness of Transfer Learning for Code Search

[![DOI](https://zenodo.org/badge/514598312.svg)](https://zenodo.org/badge/latestdoi/514598312)
[![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)
[![Netlify Status](https://api.netlify.com/api/v1/badges/4311fc80-69ec-4107-9ed6-fae874b2d2b9/deploy-status)](https://app.netlify.com/sites/tl-codesearch/deploys)

This repository represents the replication package for the paper:

> **On the Effectiveness of Transfer Learning for Code Search**
> 
> The Transformer architecture and transfer learning have marked a quantum leap in natural language processing, improving the state of the art across a range of text-based tasks. This paper examines how these advancements can be applied to and improve code search. To this end, we pre-train a BERT-based model on combinations of natural language and source code data and fine-tune it on pairs of StackOverflow question titles and code answers. Our results show that the pre-trained models consistently outperform the models that were not pre-trained. In cases where the model was pre-trained on natural language "and" source code data, it also outperforms an information retrieval baseline based on Lucene. Also, we demonstrated that the combined use of an information retrieval-based approach followed by a Transformer leads to the best results overall, especially when searching into a large search pool. Transfer learning is particularly effective when much pre-training data is available and fine-tuning data is limited. We demonstrate that natural language processing models based on the Transformer architecture can be directly applied to source code analysis tasks, such as code search. With the development of Transformer models designed more specifically for dealing with source code data, we believe the results of source code analysis tasks can be further improved.

The paper is published in the journal *IEEE Transactions on Software Engineering (TSE)*.

In our work, we design a **Multimodal Embedding Model (MEM)** architecture, which leverages the predictive capabilities of [BERT](https://github.com/google-research/bert), a state-of-the-art, _Transformer_-based _NLP_ model, and makes use of **transfer learning** to improve the performance on code search.

In this replication package, we provide all the data and scripts we used in our study.

## :open_file_folder: Organization

The repository is organized as follows:

* [`data/`](data/) contains the data of the replication package
  * [`source/`](data/source/) the source code for the pre-training and fine-tuning, and mining of *StackOverflow* data
  * [`models/`](data/models/) the pre-trained *BERT* models, ready to be loaded and used for other tasks, or to replicate the rest of our study
  * [`sodata/`](data/sodata/) the _StackOverflow_ data description and files we collected to fine-tune our _MEM_ architecture
  * [`results/`](data/results/) the results data we collected
  * [`analysis/`](data/analysis/) the full analysis we performed, in form of a _Python Jupyter Notebook_
* [`docs/`](docs/) contains the source code for the website where we documented our experiments

## :books: How to cite this dataset

If you would like to cite the dataset, please use the following `BibTeX` snippet:

```bibtex
@article{salza_transfer_2022,
    author = {Salza, Pasquale and Schwizer, Christoph and Gu, Jian and Gall, Harald C.},
    title = {{On the Effectiveness of Transfer Learning for Code Search}},
    journal = {IEEE Transactions on Software Engineering (TSE)},
    year = {2022},
}
```

## :balance_scale: License

This replication package is licensed under the terms of the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
Please see the [LICENSE](LICENSE) file for full details.

## :pray: Credits

* [Pasquale Salza](mailto:salza@ifi.uzh.ch) - University of Zurich, Switzerland
* [Christoph Schwizer](mailto:christoph@schwizer.dev) - University of Zurich, Switzerland
* [Jian Gu](mailto:gu@ifi.uzh.ch) - University of Zurich, Switzerland
* [Harald C. Gall](mailto:gall@ifi.uzh.ch) - University of Zurich, Switzerland
