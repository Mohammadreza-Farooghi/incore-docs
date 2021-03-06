# IN-CORE documents

Main IN-Core documentation which is built using Python [Sphinx](http://www.sphinx-doc.org/en/master/) package.

# Installation

1. Clone the code from INCORE docs [git](https://opensource.ncsa.illinois.edu/bitbucket/scm/incore1/incore-docs.git) 
repository.
2. Install required packages. Currently `sphinx`, a Python package for building documentation and `sphinx_rtd_theme`, 
a theme used in this documentation and other packages. See section 4. for the full list.
3. We recommend using virtual environments, `conda` (preferred) or `virtualenv` for Python 3.6+. 
for managing Python environments.  
In case of `conda`, the package management and deployment tool 
is called `anaconda`. Create the environment from the terminal at the project 
folder (called `incore_docs` here) and activate it:

    ```
    conda create -n incore_docs python=3.6 anaconda
    source activate incore_docs
    ```
    or  
    ```
    virtualenv --python=python3.6 incore_docs
    source venv/bin/activate
    ```
4. Install required packages individually if necessary. use `conda` again or  
you can also use `pip` for installing packages. Packages 2) and 3) are for correct 
rendering of the tables and 4) and 5) installs extension that provides a source parser 
for Jupyter Notebook **ipynb files**:

    ```
    conda install sphinx
    conda install sphinx_rtd_theme
    conda install recommonmark
    pip install sphinx-markdown-tables
    conda install -c conda-forge nbsphinx
    conda install -c conda-forge ipythony
    ```
    or (global install for all users drop the --user flag)
    ```
    python3 -m pip install sphinx --user
    python3 -m pip install sphinx_rtd_theme --user
    python3 -m pip install recommonmark --user
    python3 -m pip install sphinx-markdown-tables --user
    python3 -m pip install nbsphinx --user
    python3 -m pip install IPython --user
    ```   

# Running

From the terminal at the project folder (incore-docs/manual) run: 

```
sphinx-build -b html source build
```

after that you should be able to run (`clean` deletes content of the `build` folder) :

```
make clean
make html
```
            
# Testing
    NA
