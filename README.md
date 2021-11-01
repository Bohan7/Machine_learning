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
The feature engineering and models evaluations can be reproduced in:

``project1.ipynb``

Note: we change the labels from {-1, 1} to {0, 1} for our logistic regression, which can make it model the probability.

You can reproduce The training and the best prediction on the test set of the competition system:

``python run.py``


