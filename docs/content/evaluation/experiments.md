---
title: Experiments
weight: 1
katex: true
---

To evaluate the models deriving from our approach, we applied _10-fold cross-validation_ to all the experiments by splitting the entire dataset into ten equal folds and using nine for training and one for testing.
We further split the data from the nine training folds into 90 % training and 10 % validation data, leaving us with the fold sizes as approximately reported in the following table.

Language | Total | Training | Validation | Test
--- | ---: | ---: | ---: | ---:
_JavaScript_ | 85,049 | 68,889 | 7,654 | 8,504
_Java_ | 71,194 | 57,667 | 6,407 | 7,119
_Python_ | 87,231 | 70,657 | 7,850 | 8,723
_TOP_ | 243,474 | 197,213 | 21,912 | 24,347

With the number of observations from the cross-validation, we can apply statistical tests to mitigate the risk of spurious differences.

{{% notice note %}}
Since some question posts on _StackOverflow_ might be related to multiple programming languages, in order to avoid duplicates and ambiguities we removed such intersections in the case of the _TOP_ dataset.
This cleaning operation resulted into a removal of 1,145 pairs from _TOP_.
{{% /notice %}}

The following tables describe all the experiments we ran in our evaluation.
For each of the models, we indicate a label that we use as a unique reference for that model.

## Fine-tuned models

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | _JavaScript_ | _JavaScript_ | _JavaScript_ | `MEM–{NO+JS}–[JS]–(JS)`
None | _Java_ | _Java_ | _Java_ | `MEM–{NO+JA}–[JA]–(JA)`
None | _Python_ | _Python_ | _Python_ | `MEM–{NO+PY}–[PY]–(PY)`
None | _TOP_ | _JavaScript_ | _JavaScript_ | `MEM–{NO+TP}–[JS]–(JS)`
None | _TOP_ | _Java_ | _Java_ | `MEM–{NO+TP}–[JA]–(JA)`
None | _TOP_ | _Python_ | _Python_ | `MEM–{NO+TP}–[PY]–(PY)`
None | _TOP_ | _TOP_ | _TOP_ | `MEM–{NO+TP}–[TP]–(TP)`
None | _ALL_ | _JavaScript_ | _JavaScript_ | `MEM–{NO+AL}–[JS]–(JS)`
None | _ALL_ | _Java_ | _Java_ | `MEM–{NO+AL}–[JA]–(JA)`
None | _ALL_ | _Python_ | _Python_ | `MEM–{NO+AL}–[PY]–(PY)`
None | _ALL_ | _TOP_ | _TOP_ | `MEM–{NO+AL}–[TP]–(TP)`
_English_ | None | _JavaScript_ | _JavaScript_ | `MEM–{EN+NO}–[JS]–(JS)`
_English_ | None | _Java_ | _Java_ | `MEM–{EN+NO}–[JA]–(PY)`
_English_ | None | _Python_ | _Python_ | `MEM–{EN+NO}–[PY]–(PY)`
_English_ | None | _TOP_ | _TOP_ | `MEM–{EN+NO}–[TP]–(TP)`
_English_ | _JavaScript_ | _JavaScript_ | _JavaScript_ | `MEM–{EN+JS}–[JS]–(JS)`
_English_ | _Java_ | _Java_ | _Java_ | `MEM–{EN+JA}–[JA]–(JA)`
_English_ | _Python_ | _Python_ | _Python_ | `MEM–{EN+PY}–[PY]–(PY)`
_English_ | _TOP_ | _JavaScript_ | _JavaScript_ | `MEM–{EN+TP}–[JS]–(JS)`
_English_ | _TOP_ | _Java_ | _Java_ | `MEM–{EN+TP}–[JA]–(JA)`
_English_ | _TOP_ | _Python_ | _Python_ | `MEM–{EN+TP}–[PY]–(PY)`
_English_ | _TOP_ | _TOP_ | _TOP_ | `MEM–{EN+TP}–[TP]–(TP)`
_English_ | _ALL_ | _JavaScript_ | _JavaScript_ | `MEM–{EN+AL}–[JS]–(JS)`
_English_ | _ALL_ | _Java_ | _Java_ | `MEM–{EN+AL}–[JA]–(JA)`
_English_ | _ALL_ | _Python_ | _Python_ | `MEM–{EN+AL}–[PY]–(PY)`
_English_ | _ALL_ | _TOP_ | _TOP_ | `MEM–{EN+AL}–[TP]–(TP)`

## Baselines

### Random

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | None | None | _JavaScript_ | `MEM–{NO+NO}–[NO]–(JS)`
None | None | None | _Java_ | `MEM–{NO+NO}–[NO]–(JA)`
None | None | None | _Python_ | `MEM–{NO+NO}–[NO]–(PY)`
None | None | None | _TOP_ | `MEM–{NO+NO}–[NO]–(TP)`

### Zero-shot

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | _JavaScript_ | None | _JavaScript_ | `MEM–{NO+JS}–[NO]–(JS)`
None | _Java_ | None | _Java_ | `MEM–{NO+JA}–[NO]–(JA)`
None | _Python_ | None | _Python_ | `MEM–{NO+PY}–[NO]–(PY)`
None | _TOP_ | None | _JavaScript_ | `MEM–{NO+TP}–[NO]–(JS)`
None | _TOP_ | None | _Java_ | `MEM–{NO+TP}–[NO]–(JA)`
None | _TOP_ | None | _Python_ | `MEM–{NO+TP}–[NO]–(PY)`
None | _TOP_ | None | _TOP_ | `MEM–{NO+TP}–[NO]–(TP)`
None | _ALL_ | None | _JavaScript_ | `MEM–{NO+AL}–[NO]–(JS)`
None | _ALL_ | None | _Java_ | `MEM–{NO+AL}–[NO]–(JA)`
None | _ALL_ | None | _Python_ | `MEM–{NO+AL}–[NO]–(PY)`
None | _ALL_ | None | _TOP_ | `MEM–{NO+AL}–[NO]–(TP)`
_English_ | None | None | _JavaScript_ | `MEM–{EN+NO}–[NO]–(JS)`
_English_ | None | None | _Java_ | `MEM–{EN+NO}–[NO]–(PY)`
_English_ | None | None | _Python_ | `MEM–{EN+NO}–[NO]–(PY)`
_English_ | None | None | _TOP_ | `MEM–{EN+NO}–[NO]–(TP)`
_English_ | _JavaScript_ | None | _JavaScript_ | `MEM–{EN+JS}–[NO]–(JS)`
_English_ | _Java_ | None | _Java_ | `MEM–{EN+JA}–[NO]–(JA)`
_English_ | _Python_ | None | _Python_ | `MEM–{EN+PY}–[NO]–(PY)`
_English_ | _TOP_ | None | _JavaScript_ | `MEM–{EN+TP}–[NO]–(JS)`
_English_ | _TOP_ | None | _Java_ | `MEM–{EN+TP}–[NO]–(JA)`
_English_ | _TOP_ | None | _Python_ | `MEM–{EN+TP}–[NO]–(PY)`
_English_ | _TOP_ | None | _TOP_ | `MEM–{EN+TP}–[NO]–(TP)`
_English_ | _ALL_ | None | _JavaScript_ | `MEM–{EN+AL}–[NO]–(JS)`
_English_ | _ALL_ | None | _Java_ | `MEM–{EN+AL}–[NO]–(JA)`
_English_ | _ALL_ | None | _Python_ | `MEM–{EN+AL}–[NO]–(PY)`
_English_ | _ALL_ | None | _TOP_ | `MEM–{EN+AL}–[NO]–(TP)`

### No pre-train

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | None | _JavaScript_ | _JavaScript_ | `MEM–{NO+NO}–[JS]–(JS)`
None | None | _Java_ | _Java_ | `MEM–{NO+NO}–[JA]–(JA)`
None | None | _Python_ | _Python_ | `MEM–{NO+NO}–[PY]–(PY)`
None | None | _TOP_ | _TOP_ | `MEM–{NO+NO}–[TP]–(TP)`

### Lucene `v8.6.1`

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | None | None | _JavaScript_ | `LU–(JS)`
None | None | None | _Java_ | `LU–(JA)`
None | None | None | _Python_ | `LU–(PY)`
None | None | None | _TOP_ | `LU–(TP)`

### DeepCS

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | None | _JavaScript_ | _JavaScript_ | `DC–[JS]–(JS)`
None | None | _Java_ | _Java_ | `DC–[JA]–(JA)`
None | None | _Python_ | _Python_ | `DC–[PY]–(PY)`
None | None | _TOP_ | _TOP_ | `DC–[TP]–(TP)`

## Combined models

### Fine-tuned models

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | _JavaScript_ | _JavaScript_ | _JavaScript_ | `LUMEM–{NO+JS}–[JS]–(JS)`
None | _Java_ | _Java_ | _Java_ | `LUMEM–{NO+JA}–[JA]–(JA)`
None | _Python_ | _Python_ | _Python_ | `LUMEM–{NO+PY}–[PY]–(PY)`
None | _TOP_ | _JavaScript_ | _JavaScript_ | `LUMEM–{NO+TP}–[JS]–(JS)`
None | _TOP_ | _Java_ | _Java_ | `LUMEM–{NO+TP}–[JA]–(JA)`
None | _TOP_ | _Python_ | _Python_ | `LUMEM–{NO+TP}–[PY]–(PY)`
None | _TOP_ | _TOP_ | _TOP_ | `LUMEM–{NO+TP}–[TP]–(TP)`
None | _ALL_ | _JavaScript_ | _JavaScript_ | `LUMEM–{NO+AL}–[JS]–(JS)`
None | _ALL_ | _Java_ | _Java_ | `LUMEM–{NO+AL}–[JA]–(JA)`
None | _ALL_ | _Python_ | _Python_ | `LUMEM–{NO+AL}–[PY]–(PY)`
None | _ALL_ | _TOP_ | _TOP_ | `LUMEM–{NO+AL}–[TP]–(TP)`
_English_ | None | _JavaScript_ | _JavaScript_ | `LUMEM–{EN+NO}–[JS]–(JS)`
_English_ | None | _Java_ | _Java_ | `LUMEM–{EN+NO}–[JA]–(PY)`
_English_ | None | _Python_ | _Python_ | `LUMEM–{EN+NO}–[PY]–(PY)`
_English_ | None | _TOP_ | _TOP_ | `LUMEM–{EN+NO}–[TP]–(TP)`
_English_ | _JavaScript_ | _JavaScript_ | _JavaScript_ | `LUMEM–{EN+JS}–[JS]–(JS)`
_English_ | _Java_ | _Java_ | _Java_ | `LUMEM–{EN+JA}–[JA]–(JA)`
_English_ | _Python_ | _Python_ | _Python_ | `LUMEM–{EN+PY}–[PY]–(PY)`
_English_ | _TOP_ | _JavaScript_ | _JavaScript_ | `LUMEM–{EN+TP}–[JS]–(JS)`
_English_ | _TOP_ | _Java_ | _Java_ | `LUMEM–{EN+TP}–[JA]–(JA)`
_English_ | _TOP_ | _Python_ | _Python_ | `LUMEM–{EN+TP}–[PY]–(PY)`
_English_ | _TOP_ | _TOP_ | _TOP_ | `LUMEM–{EN+TP}–[TP]–(TP)`
_English_ | _ALL_ | _JavaScript_ | _JavaScript_ | `LUMEM–{EN+AL}–[JS]–(JS)`
_English_ | _ALL_ | _Java_ | _Java_ | `LUMEM–{EN+AL}–[JA]–(JA)`
_English_ | _ALL_ | _Python_ | _Python_ | `LUMEM–{EN+AL}–[PY]–(PY)`
_English_ | _ALL_ | _TOP_ | _TOP_ | `LUMEM–{EN+AL}–[TP]–(TP)`

### Random

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | None | None | _JavaScript_ | `LUMEM–{NO+NO}–[NO]–(JS)`
None | None | None | _Java_ | `LUMEM–{NO+NO}–[NO]–(JA)`
None | None | None | _Python_ | `LUMEM–{NO+NO}–[NO]–(PY)`
None | None | None | _TOP_ | `LUMEM–{NO+NO}–[NO]–(TP)`

### Zero-shot

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | _JavaScript_ | None | _JavaScript_ | `LUMEM–{NO+JS}–[NO]–(JS)`
None | _Java_ | None | _Java_ | `LUMEM–{NO+JA}–[NO]–(JA)`
None | _Python_ | None | _Python_ | `LUMEM–{NO+PY}–[NO]–(PY)`
None | _TOP_ | None | _JavaScript_ | `LUMEM–{NO+TP}–[NO]–(JS)`
None | _TOP_ | None | _Java_ | `LUMEM–{NO+TP}–[NO]–(JA)`
None | _TOP_ | None | _Python_ | `LUMEM–{NO+TP}–[NO]–(PY)`
None | _TOP_ | None | _TOP_ | `LUMEM–{NO+TP}–[NO]–(TP)`
None | _ALL_ | None | _JavaScript_ | `LUMEM–{NO+AL}–[NO]–(JS)`
None | _ALL_ | None | _Java_ | `LUMEM–{NO+AL}–[NO]–(JA)`
None | _ALL_ | None | _Python_ | `LUMEM–{NO+AL}–[NO]–(PY)`
None | _ALL_ | None | _TOP_ | `LUMEM–{NO+AL}–[NO]–(TP)`
_English_ | None | None | _JavaScript_ | `LUMEM–{EN+NO}–[NO]–(JS)`
_English_ | None | None | _Java_ | `LUMEM–{EN+NO}–[NO]–(PY)`
_English_ | None | None | _Python_ | `LUMEM–{EN+NO}–[NO]–(PY)`
_English_ | None | None | _TOP_ | `LUMEM–{EN+NO}–[NO]–(TP)`
_English_ | _JavaScript_ | None | _JavaScript_ | `LUMEM–{EN+JS}–[NO]–(JS)`
_English_ | _Java_ | None | _Java_ | `LUMEM–{EN+JA}–[NO]–(JA)`
_English_ | _Python_ | None | _Python_ | `LUMEM–{EN+PY}–[NO]–(PY)`
_English_ | _TOP_ | None | _JavaScript_ | `LUMEM–{EN+TP}–[NO]–(JS)`
_English_ | _TOP_ | None | _Java_ | `LUMEM–{EN+TP}–[NO]–(JA)`
_English_ | _TOP_ | None | _Python_ | `LUMEM–{EN+TP}–[NO]–(PY)`
_English_ | _TOP_ | None | _TOP_ | `LUMEM–{EN+TP}–[NO]–(TP)`
_English_ | _ALL_ | None | _JavaScript_ | `LUMEM–{EN+AL}–[NO]–(JS)`
_English_ | _ALL_ | None | _Java_ | `LUMEM–{EN+AL}–[NO]–(JA)`
_English_ | _ALL_ | None | _Python_ | `LUMEM–{EN+AL}–[NO]–(PY)`
_English_ | _ALL_ | None | _TOP_ | `LUMEM–{EN+AL}–[NO]–(TP)`

### No pre-train

Pre-training $E_q$ | Pre-training $E_c$ | Training | Test | Label
--- | --- | --- | --- | ---
None | None | _JavaScript_ | _JavaScript_ | `LUMEM–{NO+NO}–[JS]–(JS)`
None | None | _Java_ | _Java_ | `LUMEM–{NO+NO}–[JA]–(JA)`
None | None | _Python_ | _Python_ | `LUMEM–{NO+NO}–[PY]–(PY)`
None | None | _TOP_ | _TOP_ | `LUMEM–{NO+NO}–[TP]–(TP)`
