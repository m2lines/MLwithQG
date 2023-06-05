# Ross 2022 Machine Learning Parameterizations
An online hosted collection of tutorial notebooks on Ross 2022 machine learning subgrid parametrizations.

## Structure and Organization of the Repo
This project uses [Jupyter Book](https://jupyterbook.org/) to organize a collection of Jupyter Notebooks into a website. 

- The notebooks all live in the [notebooks](https://github.com/m2lines/MLwithQG/tree/main/notebooks) directory. Note that the outputs of execution within the notebooks are saved and are thus not executed as part of the build process.
- The table of contents is located in [\_toc.yml](https://github.com/m2lines/MLwithQG/blob/main/_toc.yml).
- The book configuration is in [\_config.yml](https://github.com/m2lines/MLwithQG/blob/main/_config.yml).
- The references are in [\_references.bib](https://github.com/m2lines/MLwithQG/blob/main/references.bib).

## Setting up the Environment

### Installing pyqg
The quickest and easiest way to install pyqg is with conda. Alternative installation instructions can be found [here](https://pyqg.readthedocs.io/en/latest/installation.html#alternatives). To install pyqg with conda, run

```bash
$ conda install -c conda-forge pyqg
```

### Installing Python Dependencies
The python packages required to run and build the notebooks are listed in the [requirements.txt](https://github.com/m2lines/MLwithQG/blob/main/requirements.txt) file. To install all dependencies, run

```bash
$ python -m pip install -r requirements.txt
```

There is an additional dependency that must be installed. We must import the following [repository](https://github.com/m2lines/pyqg_parameterization_benchmarks) as a Python package. This repository contains code that abstracts parameterizations using fully convolutional neural networks (FCNN). We can do this by following these [steps](https://github.com/m2lines/pyqg_parameterization_benchmarks).

## Building the Book

To build the book locally, you should first create and set up your environment, as described above. Then run

```bash
$ jupyter-book build .
```

When you run this command, the notebooks will be executed. The built html will be placed in `\_build/html`. To preview the book, run

```bash
$ cd _build/html
$ python -m http.server
```

## References
Ross, A., Li, Z., Perezhogin, P., Fernandez-Granda, C., & Zanna, L. (2023). Benchmarking of Machine Learning Ocean Subgrid Parameterizations in an Idealized Model. Journal of Advances in Modeling Earth Systems, 15(1), e2022MS003258. https://doi.org/10.1029/2022MS003258