# DLV


This repo is forked from https://github.com/VeriDeep/DLV 

The goal is to reproduce the results presented in CAV 2017 [paper](https://arxiv.org/abs/1610.06940).


## Environment Setup 

The following instructions are tested on Mac OS X and Debian Linux.

(0) assume `miniconda` or `anaconda` is used to setup python environment

(1) create an virtual environment (called DLV or any other name you like) using conda
```
conda create -n DLV python=2.7 theano=0.9
```

(2) activate the virtual environment
```
source activate DLV
```

(3) install packages available in conda
```
conda install matplotlib cvxopt scikit-image h5py
```

(4) install packages available in pip
```
pythonp install stopit keras==1.2.2 
```

(5) revise default keras config
```
"image_dim_ordering": "tf", ==>  "image_dim_ordering": "th", 
"backend": "tensorflow" ==>  "backend": "theano"
```

(6) export z3 python environment
```
export PYTHONPATH=~/Projects/z3/build/python/
```


## Brief instructions from the original author
(1) Installation: 

To run the program, one needs to install the following packages: 

           Python 2.7
           Theano 0.9
           Keras 1.2.2  (Note: the software currently does not work well with Keras 2.x because of image dimension ordering problems, please use a previous 1.x version)
           z3 

(2) Usage: 

Use the following command to call the program: 

           python DLV.py

Please use the file ''configuration.py'' to set the parameters for the system to run. 

