# TPC-DS Tool

This repository contains the TPC-DS Toolkit v3.2.0rc1. The full instruction is available at [How_To_Guide-DS-V2.0.0](tools/How_To_Guide-DS-V2.0.0.docx).

## Build File

The build file [may not work](https://github.com/gregrahn/tpcds-kit/issues/57) for the lastest version of GCC/G++ compiler, switch to GCC 9 and G++ 9 by running :
```
$ update-alternatives --config gcc
```
and 
```
$ update-alternatives --config g++
```
to select older version of compilers.

To build the file, go to [./tools](/tools/) and run:
```
$ make OS=LINUX
```

## Data Generation

To generate data (e.g., 1G in the `./tools/data` directory), run the following within [./tools](/tools/):
```
$ mkdir data
$ dsdgen -scale 1 -dir ./data
```

## Query Generation

To be updated.