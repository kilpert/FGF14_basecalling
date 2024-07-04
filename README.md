[![DOI](https://zenodo.org/badge/728584888.svg)](https://zenodo.org/doi/10.5281/zenodo.12655177)

# FGF14 basecalling

This [Snakemake](https://github.com/snakemake/snakemake) workflow performs basecalling for [Nanopore](https://nanoporetech.com/) sequencing runs. It was specifically testet for output of the [MinION Mk1B](https://nanoporetech.com/products/sequence/minion). 

The workflow basically uses ONT Guppy to perform the basecalling and demultiplexing. In addition, it assigns sample names to the output according to the aliases for the barcodes in the sample sheet. It runs some QC, e.g. [pycoQC](https://github.com/a-slide/pycoQC), [NanoPlot](https://github.com/wdecoster/NanoPlot), as well as some custom scripts.

## Input
The workflow uses the output folder from MinKNOW as input, i.e. *fast5* files.

In order to start the workflow the user has to:
 1. provide a sample sheet file (e.g. `sample_sheets/sample_sheet.csv`)
 2. configure the Snakemake config file (`config/config.yaml`).

## Starting the workflow
The workflow can be started by running the `run.sh` on the shell.

## Publication

Mohren et al. (2024). Advancing molecular, phenotypic and mechanistic insights of FGF14 pathogenic expansions (SCA27B). *in prep.*
