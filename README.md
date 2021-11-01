# Project 1 (EPFL Machine Learning Course CS-433)
This is a repository for all code of project 1

Members:
Bohan Wang, Ke Wang, Siran Li

Structure
=================
├── implementations.py: contains **all the implementations** required by the project

├── notes.md: general notes about the project development
├── README.md: this file :)
├── requirements.txt: contains the packages used to run the project
├── run.py: contains the **final code** to train the model
├── tests.ipynb: a notebook that contains the tests of the required implementations, that can be used as guide for usage
├── data: contains the datasets (.gitignore'd)
├── notebooks
│   ├── features_log.ipynb: contains our investigations about taking the logarithm of the features
│   ├── features_overview.ipynb: contains the exploratory data analysis phase
│   ├── logistic_regression.ipynb: contains out trials with logistic regression
│   └── ridge_regression.ipynb: contains our trials with ridge regression
└── src
    ├── helpers.py: some helper functions used by different modules
    ├── split.py: contains the function used to split the dataset into training and test sets
    ├── k_fold.py: contains the functions used for cross-validation
    ├── polynomials.py: contains the functions used to get the polynom
    ├── logistic: contains the functions used to train the logistic regression model
    │   ├── loss.py: contains the function to compute the loss
    │   ├── gradient.py: contains the function to compute the gradient
    │   ├── hessian.py: contains the function to compute the hessian
    │   ├── implementations.py: contains the **logistic regression** implementations required by the project
    │   └── sigmoid.py: contains the function to compute the sigmoid
    └── linear: contains the functions used to train the linear regression model
        ├── gradient.py: contains the function to compute the gradient
        ├── implementations.py: contains the **linear regression** implementations required by the project
        └── loss.py: contains the function to compute the loss function



Train the network
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

