# Setup

I followed the instructions of this tutorial: [Tutorial](https://medium.com/@anyuhang/setting-up-python-environment-with-anaconda-and-homebrew-8c4963604df0)

## The reusable parts

### Anaconda

``` python
# install python 3.6
conda create -n <your_virtual_env> python=3.7 anaconda
# update python
conda update python
# install package
conda install package_name
# enable the virtual env
source activate
# disable the virtual env
source deactivate
```

#### Current environments

- ml
- tensorflow_env

### Python virtualenv

``` python
# create virtual env
mkvirtualenv <your_virtualenv_name>
# deactivate
deactivate
# activate
workon <your_virtualenv_name>
```

#### Current environments

- mypython_env