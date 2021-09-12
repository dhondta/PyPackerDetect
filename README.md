[![PyPi](https://img.shields.io/pypi/v/pypackerdetect.svg)](https://pypi.python.org/pypi/pypackerdetect/)
[![Build Status](https://travis-ci.com/dhondta/pypackerdetect.svg?branch=main)](https://travis-ci.com/dhondta/pypackerdetect)
[![Python Versions](https://img.shields.io/pypi/pyversions/pypackerdetect.svg)](https://pypi.python.org/pypi/pypackerdetect/)
[![Requirements Status](https://requires.io/github/dhondta/pypackerdetect/requirements/?branch=main)](https://requires.io/github/dhondta/pypackerdetect/requirements/?branch=main)
[![Known Vulnerabilities](https://snyk.io/test/github/dhondta/pypackerdetect/badge.svg?targetFile=requirements.txt)](https://snyk.io/test/github/dhondta/pypackerdetect?targetFile=requirements.txt)
[![License](https://img.shields.io/pypi/l/pypackerdetect.svg)](https://pypi.python.org/pypi/pypackerdetect/)


## Introduction

A complete refactoring of [this project](https://github.com/cylance/PyPackerDetect) to a Python package with a console script to detect whether an executable is packed.

[pefile](https://github.com/erocarrera/pefile) is used for PE parsing. [peid](https://github.com/dhondta/peid) is used as implementation of PEiD.

## Setup

```session
$ pip3 install pypackerdetect
```

## Usage

```session
$ pypackerdetect --help
[...]
usage examples:
- pypackerdetect program.exe
- pypackerdetect program.exe -b
- pypackerdetect program.exe --low-imports --unknown-sections
- pypackerdetect program.exe --imports-threshold 5 --bad-sections-threshold 5
```

## Detection Mechanisms

- PEID signatures
- Known packer section names
- Entrypoint in non-standard section
- Threshhold of non-standard sections reached
- Low number of imports
- Overlapping entrypoint sections
