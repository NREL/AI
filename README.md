# AI


This repository serves as a collection of walkthroughs, utilities, and other resources to improve the NREL AI/ML user's quality of life, both novice and expert.

The tutorial notebooks can be run using a local installation of Juypter notebooks, or they can be run using Google Colab which does not use local resources and will typically result in faster training times. Google Colab also has many of the ML prerequisites installed.

## Installation

If you would like to run the tutorials using a local Python notebook application such as Jupyter notebooks, you can do so easily by installing a Conda environment using the included `environment.yml` file. The steps to do so are as follows:

1. Ensure you have a working Conda distribution.
2. Create a new conda environment using the environment file: `conda env create --file environment.yml`.
3. Activate the new environment: `conda activate nrel-ai`.
4. Launch jupyter-lab in terminal with `jupyter-lab` and navigate to the desired tutorial.

Once you have a working conda environment you can keep it up-to-date if there have been any changes to the `environment.yml` file with: `conda env update --name nrel-ai --file environment.yml --prune`

NOTE: You might need to run a separate `conda install jupyter` on your system which will allow conda to install a `jupyter` package that is better suited for your operating system instead of the default `conda-forge` version.

## Overview

The modern machine learning landscape is one that is divided between various packages in both Python (TensorFlow and PyTorch) and Julia. Although in recent years that has been a preference by many leading large tech companies for PyTorch, TensorFlow still remains useful for many research tasks. For scientific ML, it might be beneficial to leverage existing packages that may not be implemented in both PyTorch and TensorFlow. Therefore, each of the tutorials in the folders are implemented in TensorFlow, PyTorch, and Julia which will serve as a useful tool when considering porting existing code to a different package as needs arise.

The tutorials are divided into sections aimed at covering the wide breadth of ML techniques useful for scientific and general ML.


## Supervised Learning

Supervised machine learning tasks use **labeled** datasets to train models for predictions and classification tasks. The tutorials in this folder cover the following subjects:

### Regression

1. Artificial Neural Networks for Multidimensional Regression
    * Generating multidimensional data for testing
    * Preprocessing data for training, validation, and testing
    * Creating and training an Artificial Neural Network (ANN)
    * Visualizing and interogating the performance of the model
    * Brief overview of hyperparameters

2. Uncertainty Quantification for Multidimensional Probabilistic Regression
    * Generating multidimensional data with noise added
    * Preprocessing data
    * Creating and training an ANN, Bayesian Last Layer (BLL), and Bayesian Neural Network (BNN)
    * Evaluating the ANN, BLL, and BNN to determine the epistemic and aleatoric uncertainties
    * Visualizing and interpretting the results of the models in the context of UQ



## Unsupervised Learning

Unsupervised machine learning tasks use **unlabeled** datasets to trian models for clustering tasks.


## Reinforcement Learning

Reinforcement machine learning techniques train a model to make decisions by training in an interactive environment and is useful for a variety of optimization and control tasks.