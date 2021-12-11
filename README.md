<p align="center"><img src="https://github.com/dhondta/PyPackerDetect/raw/master/logo.png"></p>
<h1 align="center">PyPackerDetect <a href="https://twitter.com/intent/tweet?text=PyPackerDetect%20-%20Packer%20detector%20using%20multiple%20heuristics%20and%20PEiD's%20signatures%20database.%0D%0Ahttps%3a%2f%2fgithub%2ecom%2fdhondta%2fPyPackerDetect%0D%0A&hashtags=python,pe,peid,packer,packingdetection"><img src="https://img.shields.io/badge/Tweet--lightgrey?logo=twitter&style=social" alt="Tweet" height="20"/></a></h1>
<h3 align="center">Detect packers on PE files using heuristics and signatures.</h3>

[![PyPi](https://img.shields.io/pypi/v/pypackerdetect.svg)](https://pypi.python.org/pypi/pypackerdetect/)
[![Build Status](https://travis-ci.com/dhondta/pypackerdetect.svg?branch=main)](https://travis-ci.com/dhondta/pypackerdetect)
[![Python Versions](https://img.shields.io/pypi/pyversions/pypackerdetect.svg)](https://pypi.python.org/pypi/pypackerdetect/)
[![Requirements Status](https://requires.io/github/dhondta/pypackerdetect/requirements/?branch=main)](https://requires.io/github/dhondta/pypackerdetect/requirements/?branch=main)
[![Known Vulnerabilities](https://snyk.io/test/github/dhondta/pypackerdetect/badge.svg?targetFile=requirements.txt)](https://snyk.io/test/github/dhondta/pypackerdetect?targetFile=requirements.txt)
[![DOI](https://zenodo.org/badge/384872434.svg)](https://zenodo.org/badge/latestdoi/384872434)
[![License](https://img.shields.io/pypi/l/pypackerdetect.svg)](https://pypi.python.org/pypi/pypackerdetect/)


A complete refactoring of [this project](https://github.com/cylance/PyPackerDetect) to a Python package with a console script to detect whether an executable is packed.

[pefile](https://github.com/erocarrera/pefile) is used for PE parsing. [peid](https://github.com/dhondta/peid) is used as implementation of PEiD.

```session
$ pip install pypackerdetect
```

```session
$ pypackerdetect --help
[...]
usage examples:
- pypackerdetect program.exe
- pypackerdetect program.exe -b
- pypackerdetect program.exe --low-imports --unknown-sections
- pypackerdetect program.exe --imports-threshold 5 --bad-sections-threshold 5
```

## :bulb: Detection Mechanisms

- PEID signatures
- Known packer section names
- Entrypoint in non-standard section
- Threshhold of non-standard sections reached
- Low number of imports
- Overlapping entrypoint sections


## :star: Related Projects

You may also like these:

- [Awesome Executable Packing](https://github.com/dhondta/awesome-executable-packing): A curated list of awesome resources related to executable packing.
- [Bintropy](https://github.com/dhondta/bintropy): Analysis tool for estimating the likelihood that a binary contains compressed or encrypted bytes.
- [Dataset of packed ELF files](https://github.com/dhondta/dataset-packed-elf): Dataset of ELF samples packed with many different packers.
- [Dataset of packed PE files](https://github.com/dhondta/dataset-packed-pe): Dataset of PE samples packed with many different packers.
- [Docker Packing Box](https://github.com/dhondta/docker-packing-box): Docker image gathering packers and tools for making datasets of packed executables.
- [PEiD](https://github.com/dhondta/peid): Python implementation of the Packed Executable iDentifier (PEiD).


## :clap:  Supporters

[![Stargazers repo roster for @dhondta/PyPackerDetect](https://reporoster.com/stars/dark/dhondta/PyPackerDetect)](https://github.com/dhondta/PyPackerDetect/stargazers)

[![Forkers repo roster for @dhondta/PyPackerDetect](https://reporoster.com/forks/dark/dhondta/PyPackerDetect)](https://github.com/dhondta/PyPackerDetect/network/members)

<p align="center"><a href="#"><img src="https://img.shields.io/badge/Back%20to%20top--lightgrey?style=social" alt="Back to top" height="20"/></a></p>
