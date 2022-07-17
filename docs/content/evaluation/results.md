---
title: Results
weight: 2
---

We release the results `CSV` files for each of the experiments.

Type | Data
--- | ---
Results | `results.tar.xz` (md5: `6f6de4da1f6c98b31b188e829c19f293`)
|| [results.tar.xz.part.000] <br /> [results.tar.xz.part.001] <br /> [results.tar.xz.part.002] <br /> [results.tar.xz.part.003] <br /> [results.tar.xz.part.004] <br /> [results.tar.xz.part.005] <br /> [results.tar.xz.part.006] <br /> [results.tar.xz.part.007] <br /> [results.tar.xz.part.008] <br /> [results.tar.xz.part.009] <br /> [results.tar.xz.part.010] <br /> [results.tar.xz.part.011] <br /> [results.tar.xz.part.012] <br /> [results.tar.xz.part.013] <br /> [results.tar.xz.part.014]
Aroma scores | `results-aroma.tar.xz` (md5: `d9dcce739d1a4f030049ea872d9a7c17`)
|| [results-aroma.tar.xz.part.000] <br /> [results-aroma.tar.xz.part.001]

Each of the `CSV` files comprehends the following data:

Field | Description
--- | ---
`size` | The evaluation strategy, between _1k_ and _full_.
`fold` | The cross-validation fold number.
`stackoverflow_question_id` | The question ID of the _StackOverflow_ question.
`stackoverflow_answer_id` | The answer ID of the correct code snippet on _StackOverflow_.
`predicted_rank` | The rank value predicted by the model for the correct code snippet.
`predicted_distance` | The computed _cosine distance_, used to compute the rank for the correct code snippet.
`predicted_first_distance` | The _cosine distance_ computed for the instance that the model ranked as first.
`predicted_first_stackoverflow_answer_id` | The answer ID on _StackOverflow_ for the instance that the model ranked as first.
`predicted_last_distance` | The _cosine distance_ computed for the instance that the model ranked as last.
`predicted_last_stackoverflow_answer_id` | The answer ID on _StackOverflow_ for the instance that the model ranked as last.
`distance_mean` | The mean of the _cosine distance_ values computed for all the test code snippets.
`distance_std` | The standard deviation of the _cosine distance_.
`distance_min` | The minimum value of the _cosine distance_.
`distance_q1` | The first quartile of the _cosine distance_.
`distance_q2` | The second quartile (median) of the _cosine distance_.
`distance_q3` | The third quartile of the _cosine distance_.
`distance_max` | The maximum value of the _cosine distance_.
`aroma` | The aroma score value, only in `results-aroma.tar.xz`.

[results.tar.xz.part.000]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.000
[results.tar.xz.part.001]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.001
[results.tar.xz.part.002]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.002
[results.tar.xz.part.003]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.003
[results.tar.xz.part.004]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.004
[results.tar.xz.part.005]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.005
[results.tar.xz.part.006]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.006
[results.tar.xz.part.007]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.007
[results.tar.xz.part.008]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.008
[results.tar.xz.part.009]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.009
[results.tar.xz.part.010]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.010
[results.tar.xz.part.011]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.011
[results.tar.xz.part.012]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.012
[results.tar.xz.part.013]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.013
[results.tar.xz.part.014]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results.tar.xz.part.014

[results-aroma.tar.xz.part.000]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results-aroma.tar.xz.part.000
[results-aroma.tar.xz.part.001]: https://github.com/pasqualesalza/tlcs/raw/main/data/results/results-aroma.tar.xz.part.001
