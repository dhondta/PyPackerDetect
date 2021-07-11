# PyPackerDetect

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
