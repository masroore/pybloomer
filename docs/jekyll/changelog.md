---
date: '2023-04-28T09:04:53.824Z'
docname: changelog
images: {}
path: /changelog
title: Changelog
---

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.6.0](https://github.com/masroore/pybloomer/releases/tag/0.6.0) (2023-04-28)

### Changes


* Added windows support (MSVC)

## [0.5.7](https://github.com/prashnts/pybloomfiltermmap3/releases/tag/0.5.7) (2023-02-16)

### Fixes


* Ensure installation in Python 3.10+ doesn’t fail.

## [0.5.5](https://github.com/prashnts/pybloomfiltermmap3/releases/tag/0.5.5) (2021-10-28)

### Fixes


* Bad upload to PyPI (which is yanked). Everything else is the same as 0.5.4.

## [0.5.4](https://github.com/prashnts/pybloomfiltermmap3/releases/tag/0.5.4) (2021-10-28)

### Fixes


* Add a special case for bytes objects in the filter. Fixes the serialization issues when loading the filter.

### Added


* Added BitCount to get approximate count of elements in the set. (@xyb)


* Added `BloomFilter.approx_len()` and `BloomFilter.bit_count()` properties.

### Changes


* Calling len(bloomfilter) now reports approximate element count if any set union or intersection was performed.

## [0.5.3](https://github.com/prashnts/pybloomfiltermmap3/releases/tag/0.5.3) (2020-08-22)

### Fixes


* Fixed a long standing issue where Bloom filter length would not get reset after calling clear_all()


* Added C99 compatibility for MurmurHash3.c as pybloomfilter would fail on some systems such as Alpine

### Changes


* Release tooling (uploads tagged releases to pypi).

## [0.5.2](https://github.com/prashnts/pybloomfiltermmap3/releases/tag/0.5.2) (2020-01-13)

### Changes


* Python setup will now always try to use and build from Cython, if the module is available in the current environment.
To force cythonize, use “–cython”. If the module is not available and no “–cython” was used, the setup
will look for a bundled Cython source.

## [0.5.1](https://github.com/prashnts/pybloomfiltermmap3/releases/tag/0.5.1) (2019-12-31)

### Changes


* Add `BloomFilter.bit_array()` property for bit vector representation


* Add `BloomFilter.filename()` property and issue a PendingDeprecationWarning when using `BloomFilter.name()`


* Do memset after initializing BloomFilter instance to set alignment bytes to 0 prior to populating the filter (see notes in #24)


* Remove `mode` parameter from `BloomFilter.from_base64()` method introduced in 0.5.0 as part of a refactoring (see notes in #23)


* Add explicit flag to build using Cython when building or installing a package; setup looks for a bundled Cython
source by default (included in the PyPI distribution package)

## [0.5.0](https://github.com/prashnts/pybloomfiltermmap3/releases/tag/0.5.0) (2019-11-25)

### Changes


* Add support for read-only Bloom filter files


* Add customization of hash seeds for hashing algorithms


* Drop Python < 3.5 support

## [0.4.19](https://pypi.org/project/pybloomfiltermmap3/0.4.19) (2019-10-11)

### Changes


* Ensure that filename is encoded in `copy_template()` (thanks [@gonzalezzfelipe](https://github.com/gonzalezzfelipe)!)

## [0.4.18](https://pypi.org/project/pybloomfiltermmap3/0.4.18) (2019-10-08)

### Fixes


* Fix missing Cython dependency in setup.py

## [0.4.17](https://pypi.org/project/pybloomfiltermmap3/0.4.17) (2019-08-25)

### Fixes


* PyPi wants `long_description` and its type

## [0.4.16](https://pypi.org/project/pybloomfiltermmap3/0.4.16) (2019-08-25)

### Fixes


* Fix read / write of base64 encoded filter files (thanks [@gaetano-guerriero](https://github.com/gaetano-guerriero)!)

## [0.4.15](https://pypi.org/project/pybloomfiltermmap3/0.4.15) (2019-04-09)

### Changes


* Remove Python 2 support, add Python 3 support

## Previous Versions

See Python 2 [pybloomfiltermmap CHANGELOG](https://github.com/axiak/pybloomfiltermmap/blob/master/CHANGELOG).
