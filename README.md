# cluster-toy-project

## Description

This toy project is a proof of concept on how to use `{targets}` R package in Compute Canada's clusters. Most of it was created using `targets::use_targets()`, `targets::tar_renv()` and `renv::init()`.

## How to set up

First, connect to the desired cluster and `cd` into a suitable folder.

Clone the repository

```bash
git clone https://github.com/GiuseppeTT/cluster-toy-project.git
cd cluster-toy-project
```

Load R module

```bash
module load r
```

Install R packages

```bash
Rscript -e "renv::restore()"
```

## How to run

To run the pipeline, run

```bash
sbatch job.sh
```

To check the pipeline job status, run

```bash
sq
```

To check execution output messages, run

```bash
cat run.Rout
```

To clean the project, run

```bash
rm -rf _targets/ run.Rout
```
