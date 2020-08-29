# Application of Hopfield pooling on Attention-based Deep Multiple Instance Learning

This notebook demonstrates how to apply the Hopfield pooling layer. 
It is based on the PyTorch implementation of the paper [Attention-based Deep Multiple Instance Learning](https://github.com/AMLab-Amsterdam/AttentionDeepMIL) by 
* Ilse, M., Tomczak, J. M., & Welling, M. (2018). Attention-based Deep Multiple Instance Learning. [arXiv preprint arXiv:1802.04712](https://arxiv.org/pdf/1802.04712.pdf).


## Usage
* Download the PyTorch code of Attention-based Deep Multiple Instance Learning (ADMIL) from [github](https://github.com/AMLab-Amsterdam/AttentionDeepMIL).
* In the file [model.py](https://github.com/AMLab-Amsterdam/AttentionDeepMIL/blob/master/model.py#L60) of the above repo change line 60 from 
```python 
error = 1. - Y_hat.eq(Y).cpu().float().mean().data[0]
``` 
to 
```python 
error = 1. - Y_hat.eq(Y).cpu().float().mean().item()
``` 
* Set the path to the directory you copied ADMIL to in the first cell of the [mnist_bags_demo.ipynb](mnist_bags_demo.ipynb) notebook. 

* In cell 4 the parameters for the experiment can be set. Notably the model can be chosen.

* Run the notebook.


## Note
* The neural network with Hopfiled pooling, implemented in cell 2 of the [mnist_bags_demo.ipynb](mnist_bags_demo.ipynb) notebook, is based on the models proposed in ADMIL.

* The code in the [mnist_bags_demo.ipynb](mnist_bags_demo.ipynb) notebook is based on the [main.py](https://github.com/AMLab-Amsterdam/AttentionDeepMIL/blob/master/main.py) file from ADMIL.


## Disclaimer
The purpose of this notebook is merely to demonstrate how to use the Hopfield pooling layer. In no way it is intended as a comparison of the methods.  


