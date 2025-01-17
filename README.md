# DataScienceTraits.jl

[![Build Status](https://github.com/JuliaML/DataScienceTraits.jl/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/JuliaML/DataScienceTraits.jl/actions/workflows/CI.yml?query=branch%3Amain)
[![Coverage](https://codecov.io/gh/JuliaML/DataScienceTraits.jl/branch/main/graph/badge.svg)](https://codecov.io/gh/JuliaML/DataScienceTraits.jl)

This package provides an alternative implementation to
[ScientificTypes.jl](https://github.com/JuliaAI/ScientificTypes.jl)
that is lightweight, with a more sensible set of defaults for data science.
See https://github.com/JuliaAI/ScientificTypes.jl/issues/180.

## Usage

This package is intended for developers of statistical packages
that need to dispatch different algorithms depending on scientific
types:

```julia
using DataScienceTraits

reduction(::Continuous) = sum
reduction(::Categorical) = first
```

Extensions are provided for third-party types such as CoDa.jl
and CategoricalArrays.jl in order to facilitate the integration
with existing software stacks.
