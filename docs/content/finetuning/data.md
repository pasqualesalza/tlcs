---
title: Data
weight: 1
---

We produced our own dataset, consisting of question-answer pairs from _StackOverflow_ for the fine-tuning part.
We use the question's title as the natural language query and the accepted answer's code snippets as the source code document to be retrieved from the search corpus.

We publicly release the source code:

{{% button href="https://github.com/pasqualesalza/tlcs/raw/mainhttps://github.com/pasqualesalza/tlcs/raw/main/data/source/src-sodatamining.tar.xz" icon="fas fa-download" %}}src-sodatamining.tar.xz{{% /button %}}

We included the [Google BigQuery](https://cloud.google.com/bigquery) queries to mine the data and the scripts for preprocessing it.

## Description

The following table shows the number of _StackOverflow_ questions after each filtering step.
The numbers in the last row represent our final dataset sizes.

Step | _JavaScript_ | _Java_ | _Python_
--- | ---: | ---: | ---:
Questions | 2,045,114 | 1,841,296 | 1,884,571
Questions with accepted answer | 1,105,690 | 934,062 | 984,989
Accepted answer contains a code snippet | 861,273 | 533,217 | 655,430
3+ upvotes and 3+ lines of code | **85,049** | **71,194** | **87,231**

We also report the dataset quality statistics on average before and after filtering.

Language || Question upvotes | Question length (tokens) | Answer upvotes | Answer length (tokens) | Answer length (lines)
--- | --- | ---: | ---: | ---: | ---: | ---:
_JavaScript_ | Before | 2.94 | 8.74 | 4.75 | 175.61 | 29.73
|| **After** | **21.16** | **8.48** | **28.96** | **207.39** | **34.43**
_Java_ | Before | 3.18 | 8.62 | 5.14 | 203.50 | 29.64
|| **After** | **16.64** | **8.49** | **22.61** | **262.99** | **37.73**
_Python_ | Before | 3.51 | 9.08 | 5.34 | 165.15 | 25.89
|| **After** | **18.37** | **8.66** | **24.13** | **205.90** | **32.63**

## Mined data

We release the mined data in the form of `JSON Lines` files.

Each of the lines contains the fields `fold_x`, where `x` is the fold number.
For each of them, a value among `train`, `valid`, and `test` is specified to indicate to which set that line is belonging in the case of that fold.

Language | Size | Data
--- | ---: | ---
_JavaScript_ | 85,049 | [sodata-js.jsonl.xz]
_Java_ | 71,194 | [sodata-ja.jsonl.xz]
_Python_ | 87,231 | [sodata-py.jsonl.xz]

[sodata-js.jsonl.xz]: https://github.com/pasqualesalza/tlcs/raw/main/data/sodata/sodata-js.jsonl.xz
[sodata-ja.jsonl.xz]: https://github.com/pasqualesalza/tlcs/raw/main/data/sodata/sodata-ja.jsonl.xz
[sodata-py.jsonl.xz]: https://github.com/pasqualesalza/tlcs/raw/main/data/sodata/sodata-py.jsonl.xz
