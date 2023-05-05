# AutoGP.jl

[![Documentation](https://img.shields.io/badge/docs-latest-blue.svg)](https://fsaad.github.io/AutoGP.jl)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/fsaad/AutoGP.jl/ContinuousIntegration.yml?branch=master)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/fsaad/AutoGP.jl)
![License](https://img.shields.io/github/license/fsaad/AutoGP.jl?color=lightgrey)


This package contains the Julia reference implementation of AutoGP, a
method for automatically discovering models of 1D time series data using
Gaussian processes, as described in

> _Sequential Monte Carlo Learning for Time Series Structure Discovery_.<br/>
> Saad, F A; Patton, B J; Hoffmann, M D.; Saurous, R A; Mansinghka, V K.<br/>
> ICML 2023: Proc. The 40th International Conference on Machine Learning.

## Installing

The package can be added using the Julia package manager. From the Julia
REPL (version 1.8+), type `]` to enter the Pkg REPL mode and run

```
pkg> add AutoGP
```

## Developer Notes

#### Building Documentation Locally

```
$ julia --project=. docs/make.jl
$ python3 -m http.server --directory docs/build/ --bind localhost 9090
```

#### Running Tutorials

1. Obtain [Julia 1.8](https://julialang.org/downloads/) or later.
2. Clone this repository.
3. Set environment variable: `export JULIA_PROJECT=/path/to/AutoGP.jl`
4. Instantiate dependencies: `julia -e 'using Pkg; Pkg.instantiate()'`
5. Build PyCall: `PYTHON= julia -e 'using Pkg; Pkg.build("PyCall")'`
6. Verify import works: `julia -e 'import AutoGP; import PyPlot; println("success!")'`

## Citation

```bibtex
@inproceedings{saad2023icml,
title        = {Sequential Monte Carlo Learning for Time Series Structure Discovery},
author       = {Saad, Feras A. and Patton, Brian J. and Hoffmann, Matthew D. and Saurous, Rif A. and Mansinghka, V. K.},
booktitle    = {Proceedings of the 40th International Conference on Machine Learning},
series       = {Proceedings of Machine Learning Research},
fvolume      = {},
fpages       = {},
year         = {2023},
publisher    = {PMLR},
}
```
