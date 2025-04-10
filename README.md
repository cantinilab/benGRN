# bengrn

[![codecov](https://codecov.io/gh/jkobject/benGRN/branch/main/graph/badge.svg?token=benGRN_token_here)](https://codecov.io/gh/jkobject/benGRN)
[![CI](https://github.com/jkobject/benGRN/actions/workflows/main.yml/badge.svg)](https://github.com/jkobject/benGRN/actions/workflows/main.yml)
[![PyPI version](https://badge.fury.io/py/benGRN.svg)](https://badge.fury.io/py/benGRN)
[![Downloads](https://pepy.tech/badge/benGRN)](https://pepy.tech/project/benGRN)
[![Downloads](https://pepy.tech/badge/benGRN/month)](https://pepy.tech/project/benGRN)
[![Downloads](https://pepy.tech/badge/benGRN/week)](https://pepy.tech/project/benGRN)
[![GitHub issues](https://img.shields.io/github/issues/jkobject/benGRN)](https://img.shields.io/github/issues/jkobject/benGRN)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![DOI](https://zenodo.org/badge/731249338.svg)](https://doi.org/10.5281/zenodo.10573209)

Benchmark your gene regulatory networks inference algorithm (from scRNAseq or bulk RNAseq dataset) with BenGRN


<img src="bengrn.png" width="400"/>

The package is supposed to work with [GRnnData](https://cantinilab.github.io/GRnnData/) and only uses biological ground truth datasets.

It can run Genie3 & pyscenic on your data as a comparison

It has 3 main different types of key ground truth data to compare your GRN to:

- Mc Calla et al.'s ChIP+Perturb ground truth
- omnipath's literature curated ground truth
- genome wide perturb seq 's dataset 

You can find the documentation [here](https://www.jkobject.com/benGRN/)

## Install it from PyPI

```bash
pip install bengrn
```

### Install it locally and run the notebooks:

```bash
git clone https://github.com/jkobject/benGRN.git
pip install -e benGRN
```

## Usage

```py
from bengrn import BenGRN
from bengrn import some_test_function

# a GRN in grnndata formart
grndata

BenGRN(grndata).do_tests()
#or
some_test_function(grndata)
```

see the notebooks in [docs](https://www.jkobject.com/benGRN/):

1. [omnipath](https://www.jkobject.com/benGRN/notebooks/bench_omni_genie3)
2. [genome wide perturb seq](https://www.jkobject.com/benGRN/notebooks/bench_perturbseq_genie3_transp/)
3. [Mc Calla](https://www.jkobject.com/benGRN/notebooks/bench_sroy_genie3_transp/)

## /!\ offline mode

If you want to run the notebooks offline, you need to download the data first.

```python
from bengrn import download_perturb_gt, download_GT_db, download_sroy_gt

download_perturb_gt()

```

## Development

Read the [CONTRIBUTING.md](CONTRIBUTING.md) file.

Awesome Benchmark of Gene Regulatory Networks created by @jkobject
