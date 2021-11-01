# Project 1 (EPFL Machine Learning Course CS-433)
This is a repository for all code of project 1

Members:
Bohan Wang (321293)

Ke Wang 

Siran Li

Structure
=================
**implementations.py:** contains **all function implementations** required by the project

**project1.ipynb:** contains all our work on feature engineering, cross validation and models evaluations

**run.py:** contains the code to produce exactly the same .csv predictions which we used in our best submission to the competition system.

Instuctions
=================
The feature engineering and models evaluations can be reproduced in::

``project1.ipynb``

Note: we change the labels [-1, 1] into [0, 1] for our logistic regression, which can 



Best submission
=================

To train the network, you can execute the following command::

   python train_main.py --config configs/resnet_default.yml --label any-name-you-want-as-label

If you want to call for CIFAR100, you can directly do that by using the ``resnet18_cifar100.yml`` yml file. 

**Changing the dataset:** You can change the dataset by changing the name of the ``dataset/db`` field (in the yml). The datasets that exist by default in PyTorch, e.g., CIFAR10/CIFAR100/MNIST, are automatically downloaded if they do not exist. They are exported in the path ``dataset/root`` (which is set to ``/tmp/``).

**Changing the resnet model:** You have two options: a) change the ``model/name`` (in the yml) to the resnet you want, e.g., ResNet34, b) change the ``model/name`` to ``ResNetnew`` and specify the number of of blocks with the argument ``num_blocks``.


The resnet model used in Π-nets paper is the one in ``configs/resnet_pi-net.yml``. 

Apart from PyTorch, the code depends on Pyaml [2]_.


References
==========

.. [1] https://github.com/kuangliu/pytorch-cifar

.. [2] https://pypi.org/project/pyaml/

