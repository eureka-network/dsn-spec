# Decentralised Search Network specification

This repository is a stub. It is intended to capture speficiations (and their iterations) for the Decentralised Search protocol and Network (working name "DSN").

There are currently three main work streams, building
- a reproducible search node (RSN)
- an accountable search node (ASN)
- and query transformations

## Layout

The root of this repositry contains the following directories:
- `spec` contains markdown files of the active(latest) version of specification documents
- `src` contains Python3 scripts as executable specification documents, where relevant
- `tests` contains Python tests of the executable specification documents

## Using Conda as environment (optional)

Setup with Conda 23.1.0 and Python3 v3.10.6

in a terminal create an environment with
```
conda update conda

conda env create -f environment.yml
```

activate the environment with
```
conda activate dsn-spec
```