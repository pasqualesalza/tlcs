---
title: Models
weight: 3
katex: true
---

## Performance

We pre-trained the $\text{BERT}$ models, obtaining the following steps and time, and model performance.

Language | Steps | Time (days) | $MCM_{PT}$ (%) | $NLP_{PT}$ (%)
--- | ---: | ---: | ---: | ---:
_JavaScript_ | 32,3665 | 4 | 90 | 98
_Java_ | 190,662 | 2.4 | 87 | 96
_Python_ | 127,339 | 1.6 | 86 | 98
_TOP_ | 641,725 | 8 | 88 | 95
_ALL_ | 883,468 | 11 | 88 | 95

## Models data

We share the pre-trained $\text{BERT}$ models to be used as encoders for other downstream tasks.

Our models are compatible with the source code for $\text{BERT}$ by _Google_, whose source code can be found at https://github.com/google-research/bert.

Every archive file is split into partial files.
You can obtain a single file by executing the command:

```bash
cat bertc-js.tar.xz.part.* > bertc-js.tar.xz
```

Language | Data
--- | ---
_JavaScript_ | `bertc-js.tar.xz` (md5: `39e9baf0aeb2811a2e83c830d7df058d`)
|| <li> [bertc-js.tar.xz.part.000] <li> [bertc-js.tar.xz.part.001] <li> [bertc-js.tar.xz.part.002] <li> [bertc-js.tar.xz.part.003] <li> [bertc-js.tar.xz.part.004] <li> [bertc-js.tar.xz.part.005] <li> [bertc-js.tar.xz.part.006] <li> [bertc-js.tar.xz.part.007] <li> [bertc-js.tar.xz.part.008] <li> [bertc-js.tar.xz.part.009] <li> [bertc-js.tar.xz.part.010] <li> [bertc-js.tar.xz.part.011]
_Java_ | `bertc-ja.tar.xz` (md5: `5eb4217c8b3064d6fd48d481ea09c422`)
|| <li> [bertc-ja.tar.xz.part.000] <li> [bertc-ja.tar.xz.part.001] <li> [bertc-ja.tar.xz.part.002] <li> [bertc-ja.tar.xz.part.003] <li> [bertc-ja.tar.xz.part.004] <li> [bertc-ja.tar.xz.part.005] <li> [bertc-ja.tar.xz.part.006] <li> [bertc-ja.tar.xz.part.007] <li> [bertc-ja.tar.xz.part.008] <li> [bertc-ja.tar.xz.part.009] <li> [bertc-ja.tar.xz.part.010] <li> [bertc-ja.tar.xz.part.011]
_Python_ | `bertc-py.tar.xz` (md5: `9209c746c3bd6cff7bf9fe747b1c76a6`)
|| <li> [bertc-py.tar.xz.part.000] <li> [bertc-py.tar.xz.part.001] <li> [bertc-py.tar.xz.part.002] <li> [bertc-py.tar.xz.part.003] <li> [bertc-py.tar.xz.part.004] <li> [bertc-py.tar.xz.part.005] <li> [bertc-py.tar.xz.part.006] <li> [bertc-py.tar.xz.part.007] <li> [bertc-py.tar.xz.part.008] <li> [bertc-py.tar.xz.part.009] <li> [bertc-py.tar.xz.part.010] <li> [bertc-py.tar.xz.part.011]
_TOP_ | `bertc-tp.tar.xz` (md5: `e54c741a74ef135cd8031ea14f124962`)
|| <li> [bertc-tp.tar.xz.part.000] <li> [bertc-tp.tar.xz.part.001] <li> [bertc-tp.tar.xz.part.002] <li> [bertc-tp.tar.xz.part.003] <li> [bertc-tp.tar.xz.part.004] <li> [bertc-tp.tar.xz.part.005] <li> [bertc-tp.tar.xz.part.006] <li> [bertc-tp.tar.xz.part.007] <li> [bertc-tp.tar.xz.part.008] <li> [bertc-tp.tar.xz.part.009] <li> [bertc-tp.tar.xz.part.010] <li> [bertc-tp.tar.xz.part.011]
_ALL_ | `bertc-al.tar.xz` (md5: `7cc0c2911f46e2a1e291d57c1646142d`)
|| <li> [bertc-al.tar.xz.part.000] <li> [bertc-al.tar.xz.part.001] <li> [bertc-al.tar.xz.part.002] <li> [bertc-al.tar.xz.part.003] <li> [bertc-al.tar.xz.part.004] <li> [bertc-al.tar.xz.part.005] <li> [bertc-al.tar.xz.part.006] <li> [bertc-al.tar.xz.part.007] <li> [bertc-al.tar.xz.part.008] <li> [bertc-al.tar.xz.part.009] <li> [bertc-al.tar.xz.part.010] <li> [bertc-al.tar.xz.part.011]

[bertc-js.tar.xz.part.000]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.000
[bertc-js.tar.xz.part.001]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.001
[bertc-js.tar.xz.part.002]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.002
[bertc-js.tar.xz.part.003]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.003
[bertc-js.tar.xz.part.004]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.004
[bertc-js.tar.xz.part.005]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.005
[bertc-js.tar.xz.part.006]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.006
[bertc-js.tar.xz.part.007]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.007
[bertc-js.tar.xz.part.008]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.008
[bertc-js.tar.xz.part.009]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.009
[bertc-js.tar.xz.part.010]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.010
[bertc-js.tar.xz.part.011]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-js.tar.xz.part.011

[bertc-ja.tar.xz.part.000]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.000
[bertc-ja.tar.xz.part.001]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.001
[bertc-ja.tar.xz.part.002]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.002
[bertc-ja.tar.xz.part.003]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.003
[bertc-ja.tar.xz.part.004]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.004
[bertc-ja.tar.xz.part.005]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.005
[bertc-ja.tar.xz.part.006]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.006
[bertc-ja.tar.xz.part.007]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.007
[bertc-ja.tar.xz.part.008]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.008
[bertc-ja.tar.xz.part.009]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.009
[bertc-ja.tar.xz.part.010]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.010
[bertc-ja.tar.xz.part.011]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-ja.tar.xz.part.011

[bertc-py.tar.xz.part.000]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.000
[bertc-py.tar.xz.part.001]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.001
[bertc-py.tar.xz.part.002]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.002
[bertc-py.tar.xz.part.003]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.003
[bertc-py.tar.xz.part.004]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.004
[bertc-py.tar.xz.part.005]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.005
[bertc-py.tar.xz.part.006]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.006
[bertc-py.tar.xz.part.007]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.007
[bertc-py.tar.xz.part.008]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.008
[bertc-py.tar.xz.part.009]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.009
[bertc-py.tar.xz.part.010]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.010
[bertc-py.tar.xz.part.011]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-py.tar.xz.part.011

[bertc-tp.tar.xz.part.000]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.000
[bertc-tp.tar.xz.part.001]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.001
[bertc-tp.tar.xz.part.002]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.002
[bertc-tp.tar.xz.part.003]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.003
[bertc-tp.tar.xz.part.004]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.004
[bertc-tp.tar.xz.part.005]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.005
[bertc-tp.tar.xz.part.006]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.006
[bertc-tp.tar.xz.part.007]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.007
[bertc-tp.tar.xz.part.008]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.008
[bertc-tp.tar.xz.part.009]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.009
[bertc-tp.tar.xz.part.010]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.010
[bertc-tp.tar.xz.part.011]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-tp.tar.xz.part.011

[bertc-al.tar.xz.part.000]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.000
[bertc-al.tar.xz.part.001]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.001
[bertc-al.tar.xz.part.002]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.002
[bertc-al.tar.xz.part.003]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.003
[bertc-al.tar.xz.part.004]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.004
[bertc-al.tar.xz.part.005]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.005
[bertc-al.tar.xz.part.006]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.006
[bertc-al.tar.xz.part.007]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.007
[bertc-al.tar.xz.part.008]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.008
[bertc-al.tar.xz.part.009]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.009
[bertc-al.tar.xz.part.010]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.010
[bertc-al.tar.xz.part.011]: https://github.com/pasqualesalza/tlcs/raw/main/data/models/bertc-al.tar.xz.part.011
