# Running Sarek on O2

## Installation

Assumes you are working on O2. Before installing and running Nextflow
the Java module must be loaded.

```bash
module load java/jdk-11.0.11
```

### Nextflow

Use the [MCMICRO instructions](https://mcmicro.org/tutorial/installation.html)
to install Nextflow.

### Sarek

```bash
nextflow pull nf-core/sarek
```

Copy `o2.config` from this repository to your home directory on O2.

## Running Sarek

Create a sample sheet CSV file following the [nf-core/sarek instructions](https://nf-co.re/sarek/3.4.0/docs/usage#input-sample-sheet-configurations) and save it in your working directory on O2 scratch.

Create a json file with the run parameters using the [nf-core Launch pipeline feature](https://nf-co.re/launch) and save it as `nf-params.json` in your working directory on O2 scratch.

Launch the pipeline using the following command:

```bash
sbatch run_sarek.sh
```

To resume a previously launched pipeline:

```bash
sbatch run_sarek.sh -resume
```
