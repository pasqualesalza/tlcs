---
title: Data
weight: 1
katex: true
---

We pre-trained our custom $\text{BERT}$ models by using the data from the [**CodeSearchNet**](https://github.com/github/CodeSearchNet) challenge project.
The datasets are freely available.

The following table reports the size of the pre-training datasets and the links to download the datasets.
We report in bold the language datasets, or their combinations, we used to produce the pre-trained models.

Language | Number of functions | Number of tokens | Data
--- | ---: | ---: | ---
**_JavaScript_** | **1,857,835** | **128,430,003** | <li> [javascript.zip]
**_Java_** | **1,569,889** | **75,654,447** | <li> [java.zip]
**_Python_** | **1,156,085** | **50,551,794** | <li> [python.zip]
_PHP_ | 977,821 | 53,352,522 | <li> [php.zip]
_Go_ | 726,768 | 37,075,579 | <li> [go.zip]
_Ruby_ | 164,048 | 5,495,442 | <li> [ruby.zip]
**_TOP_** | **4,583,809** | **254,636,244** | <li> [javascript.zip] <li> [java.zip] <li> [python.zip]
**_ALL_** | **6,452,446** | **350,559,787** | <li> [javascript.zip] <li> [java.zip] <li> [python.zip] <li> [php.zip] <li> [go.zip] <li> [ruby.zip]

[javascript.zip]: https://s3.amazonaws.com/code-search-net/CodeSearchNet/v2/javascript.zip
[java.zip]: https://s3.amazonaws.com/code-search-net/CodeSearchNet/v2/java.zip
[python.zip]: https://s3.amazonaws.com/code-search-net/CodeSearchNet/v2/python.zip
[php.zip]: https://s3.amazonaws.com/code-search-net/CodeSearchNet/v2/php.zip
[go.zip]: https://s3.amazonaws.com/code-search-net/CodeSearchNet/v2/go.zip
[ruby.zip]: https://s3.amazonaws.com/code-search-net/CodeSearchNet/v2/ruby.zip
