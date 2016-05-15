# PyMC Examples

_Personal Project for PyMC Development_


A set of notebooks intended to demo some capabilities of nonparametric Bayesian
analysis using Python tools. In particular the `pymc3` and `emcee` toolkits.


## Development:

### Git clone the repo to your workspace.

e.g. in Mac OSX terminal:

        $> git clone https://github.com/jonsedar/pymc_examples.git
        $> cd pymc_examples



### Setup a virtual environment for Python libraries

**NOTE:** using Python 3.5

Using Anaconda distro,

1. create a new virtual env, installing packages from env YAML file:


        $> conda env create --file conda_env_pymc_examples.yml
        $> source activate pymc_examples



2. install latest builds of pymc3 and theano dev via pip:

        $> pip install --process-dependency-links git+https://github.com/pymc-devs/pymc3


3. install emcee via pip

        $> pip install emcee



---



## Data

Local data is not stored in the repo, and should be manually copied into the subdirectory data/

See file `data/README_DATA.md` for more info


---


## General Notes:

File `find_MAP_HACK.py` contains customised `find_MAP()` function to correct
for pymc3's default behaviour of computing gradients even when the chosen
optimizer doesn't use them. We don't want to compute gradients in large
datasets because it's computationally expensive.
This is a temporary hack before I try to fix properly.

