[tests-badge]: https://img.shields.io/github/actions/workflow/status/conda/conda-build/tests.yml?branch=main&event=schedule&logo=github&label=tests
[codecov-badge]: https://img.shields.io/codecov/c/github/conda/conda-build/main?logo=codecov
[codspeed-badge]: https://img.shields.io/endpoint?url=https://codspeed.io/badge.json
[release-badge]: https://img.shields.io/github/v/release/conda/conda?logo=github
[anaconda-badge]: https://img.shields.io/conda/vn/anaconda/conda-build?logo=anaconda
[conda-forge-badge]: https://img.shields.io/conda/vn/conda-forge/conda-build?logo=conda-forge
[calver-badge]: https://img.shields.io/badge/calver-YY.MM.MICRO-22bfda.svg

# `conda-build`

[![GitHub Scheduled Tests][tests-badge]](https://github.com/conda/conda-build/actions/workflows/tests.yml?query=branch%3Amain+event%3Aschedule)
[![Codecov Status][codecov-badge]](https://codecov.io/gh/conda/conda-build/branch/main)
[![CodSpeed Performance Benchmarks][codspeed-badge]](https://codspeed.io/conda/conda-build)
[![CalVer Versioning][calver-badge]](https://calver.org)
<br>
[![GitHub Release][release-badge]](https://github.com/conda/conda-build/releases)
[![Anaconda Package][anaconda-badge]](https://anaconda.org/anaconda/conda-build)
[![conda-forge Package][conda-forge-badge]](https://anaconda.org/conda-forge/conda-build)

## Installation

```bash
# Display information about current conda install
$ conda info

# Install conda-build in the base env
$ conda install -n base conda-build
```

## Building Your Own Packages

You can easily build your own packages for `conda`, and upload them to
[anaconda.org](https://anaconda.org), a free service for hosting packages for `conda`, as
well as other package managers. To build a package, create a recipe. See
[AnacondaRecipes](https://github.com/AnacondaRecipes) and [conda-forge](https://github.com/conda-forge) for many example recipes, and
[`conda-build` documentation](https://docs.conda.io/projects/conda-build/en/latest/index.html) on how to build
recipes.

To upload to [anaconda.org](https://anaconda.org), create an account.  Then, install the `anaconda-client`
and login

```bash
$ conda install anaconda-client
$ anaconda login
```

Then, after you build your recipe

```bash
$ conda build <RECIPE_DIR>
```

you will be prompted to upload to [anaconda.org](https://anaconda.org).

To add your [anaconda.org](https://anaconda.org) channel, or the channel of others to `conda` so that `conda install`
will find and install their packages, run

```bash
$ conda config --add channels https://conda.anaconda.org/<USERNAME>
```

(replacing `USERNAME` with the user name of the person whose channel you want
to add).

## Gotchas/FAQ

* `OSError: [Errno 36] File name too long:` - This error has been seen on Linux computers with encrypted folders. The solution is to install `miniconda` or `anaconda` to a location that is not encrypted. This error occurs because the encrypted form of the path that `conda-build` creates can be too long.

## Getting Help

- [Documentation](https://docs.conda.io/projects/conda-build/en/latest)
- [Twitter](https://twitter.com/condaproject)
- [Slack](https://conda.slack.com)
- [Bug Reports/Feature Requests](https://github.com/conda/conda-build/issues)
- [Installer/Package Issues](https://github.com/ContinuumIO/anaconda-issues/issues)

## Contributing

Contributions to conda-build are welcome. See the [contributing](CONTRIBUTING.md) documentation
for instructions on setting up a development environment.
