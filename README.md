About ticcltools
================

Home: https://github.com/LanguageMachines/ticcltools

Package license: GPL-3.0

Feedstock license: BSD 3-Clause

Summary: Tools for TICCL: Text Induced Corpus-Cleanup

TicclTools is a collection of programs to process datafiles, together they constitute the bulk of TICCL: Text Induced Corpus-Cleanup.
The main programs in this colection are:
* TICCL-indexer and TICCL-indexerNT:
  a tool to create an exhaustive index to all lexical variants given a particular Levenshtein or edit distance in a corpus.
* TICCL-anahash:
  a tool to create anagram hashes form a word frequency file. Also creates ab 'alphabet' file of the unicode characters that are present in the corpus.
* TICCL-LDcalc:
  a proprocessing tool for TICCL-rank. Gathers the info from TICC-anahash, TICCL-indexer, TICCL-lexstat and TICCL-unk
* TICCL-rank:
  ranks a word varian list according to al lot of criteria
* TICCL-unk:
  a cleanup tool for word frequency lists. creates a 'clean' file with desirable words, an 'unk' file with uncorrectable words and a 'punct' file with words that would be clean after removing puncuation.
* TICCL-lexstat:
  convert an 'alphabet' file (from TICCL-anahash) into a frequency list of hashes and optionally a list of confusions.


Current build status
====================


<table>
    
  <tr>
    <td>Azure</td>
    <td>
      <details>
        <summary>
          <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=6119&branchName=master">
            <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/ticcltools-feedstock?branchName=master">
          </a>
        </summary>
        <table>
          <thead><tr><th>Variant</th><th>Status</th></tr></thead>
          <tbody><tr>
              <td>linux</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=6119&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/ticcltools-feedstock?branchName=master&jobName=linux&configuration=linux_" alt="variant">
                </a>
              </td>
            </tr><tr>
              <td>osx</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=6119&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/ticcltools-feedstock?branchName=master&jobName=osx&configuration=osx_" alt="variant">
                </a>
              </td>
            </tr>
          </tbody>
        </table>
      </details>
    </td>
  </tr>
  <tr>
    <td>Windows</td>
    <td>
      <img src="https://img.shields.io/badge/Windows-disabled-lightgrey.svg" alt="Windows disabled">
    </td>
  </tr>
![ppc64le disabled](https://img.shields.io/badge/ppc64le-disabled-lightgrey.svg)
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-ticcltools-green.svg)](https://anaconda.org/conda-forge/ticcltools) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/ticcltools.svg)](https://anaconda.org/conda-forge/ticcltools) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/ticcltools.svg)](https://anaconda.org/conda-forge/ticcltools) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/ticcltools.svg)](https://anaconda.org/conda-forge/ticcltools) |

Installing ticcltools
=====================

Installing `ticcltools` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `ticcltools` can be installed with:

```
conda install ticcltools
```

It is possible to list all of the versions of `ticcltools` available on your platform with:

```
conda search ticcltools --channel conda-forge
```


About conda-forge
=================

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating ticcltools-feedstock
=============================

If you would like to improve the ticcltools recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/ticcltools-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@egpbos](https://github.com/egpbos/)
* [@jvdzwaan](https://github.com/jvdzwaan/)
* [@martinreynaert](https://github.com/martinreynaert/)

