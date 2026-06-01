# Shell-Domain Scaling Framework — Supplemental Notebook

This repository contains the supplemental notebook for:

**Shell-Domain Scaling: An Integer-Only Framework for Eliminating Floating-Point Failure Modes**
Kenneth John Rumments
Zenodo DOI: `10.5281/zenodo.20289163`

This notebook provides executable demonstrations supporting the Shell-Domain Scaling (SDS) paper. SDS represents numerical values using integer-scaled domains rather than binary floating-point arithmetic, allowing selected computations to be tested under exact or controlled integer representations.

## Purpose

The notebook demonstrates how SDS behaves on common floating-point failure modes, including:

* rounding drift from repeated operations
* decimal equality failures such as `0.1 + 0.2`
* catastrophic cancellation
* reversible add/subtract tests
* subnormal collapse comparison
* logarithm/root-related boundary behavior
* representation-dependent trajectory drift near a Mandelbrot boundary

The examples are intended to show where integer-scaled arithmetic can preserve exact representable values, avoid accumulated floating-point drift, or expose representation-dependent behavior.

## Related Work

This work builds on the companion Root Shell paper:

**Root Shell Mathematics: An Integer-Only Method for Integer k-th Root Bracketing and Refinement**
Zenodo DOI: `10.5281/zenodo.20291013`

Root Shell Mathematics defines the integer shell/root framework that supports later SDS constructions.

## Files

Primary notebook:

```text
Shell Domain Scaling Framework Supplemental.ipynb
```

Recommended supporting files:

```text
README.md
LICENSE
```

## Requirements

The notebook is designed to run in standard Python environments, including Google Colab.

Typical requirements:

```text
Python 3.x
decimal
fractions
math
time
```

No GPU is required.

## How to Run

Open the notebook in Google Colab, Jupyter Notebook, or JupyterLab.

Run the cells from top to bottom.

Some tests may use large iteration counts. The Mandelbrot boundary test may take longer depending on the machine and should be interpreted as a trajectory-sensitivity demonstration, not as a claim that SDS prevents mathematical escape.

## Important Scope Notes

SDS does not claim to represent arbitrary real numbers exactly with finite integers.

The exactness claims apply to values representable inside the chosen integer-scaled domain.

Addition and subtraction are exact under compatible scale choices and sufficient integer capacity.

Multiplication may require denominator growth, exact rescaling, or domain-specific handling.

Reversibility applies to operations that are invertible within the chosen integer representation.

The Mandelbrot boundary example demonstrates representation-dependent trajectory divergence near a sensitive boundary. It does not claim that SDS prevents escape for points that are mathematically outside the set.

## License

Recommended license for the code and notebook:

```text
Apache License 2.0
```

Recommended license for the paper text:

```text
Creative Commons Attribution 4.0 International
```

## Citation

If citing this work, use:

```text
Rumments, K. J. Shell-Domain Scaling: An Integer-Only Framework for Eliminating Floating-Point Failure Modes. Zenodo. https://doi.org/10.5281/zenodo.20289163
```

For the companion root-shell method, cite:

```text
Rumments, K. J. Root Shell Mathematics: An Integer-Only Method for Integer k-th Root Bracketing and Refinement. Zenodo. https://doi.org/10.5281/zenodo.20291013
```

## Author

Kenneth John Rumments
Independent Researcher
ORCID: `0009-0001-0924-1850`
