# generalized-cnn-xray-tuning

Code, notebooks, and dataset links for the paper: **"A Generalized Approach to CNN Layer Tuning for X-ray Medical Imaging"**.

This repository provides resources to reproduce the results presented in the paper, where Bayesian Optimization was used to find optimal custom CNN layers added to a frozen ResNet50 base for diverse X-ray classification tasks (Tuberculosis, MURA, Osteoarthritis).

## Notebooks

These notebooks contain the code used for optimization and model training/evaluation. They are designed to run on Kaggle.

* **[Bayesian Optimization (Optuna)](https://www.kaggle.com/code/nicholasnevank/bayesianoptimization-cnn):** Performs the hyperparameter search using Optuna to find the best custom layer configuration for the ResNet50 base. Generates the `optuna-study` and `bo-best-hyperparameters` datasets (see below).
* **[ResNet50 Base Training](https://www.kaggle.com/code/nicholasnevank/resnet50-cnn):** Trains and evaluates the model using the optimized hyperparameters on the ResNet50 base architecture.
* **[VGG-19 Base Training](https://www.kaggle.com/code/nicholasnevank/vgg19-cnn):** Trains and evaluates the model using the VGG-19 base architecture (used for generalizability testing).
* **[InceptionV3 Base Training](https://www.kaggle.com/code/nicholasnevank/inceptionv3-cnn):** Trains and evaluates the model using the InceptionV3 base architecture (used for generalizability testing).

## Output Datasets

Datasets generated during the Bayesian Optimization process:

* **[Optuna Study Progress](https://www.kaggle.com/datasets/nicholasnevank/optuna-study):** Contains the logs and progress details from the Optuna optimization trials.
* **[Best Hyperparameters (JSON)](https://www.kaggle.com/datasets/nicholasnevank/bo-best-hyperparameters):** A JSON file storing the best hyperparameter configuration found by the optimization.

## Input Datasets

The original X-ray datasets used for training and evaluation (hosted on Kaggle):

* **[Osteoarthritis Knee X-ray Dataset](https://www.kaggle.com/datasets/gauravduttakiit/osteoarthritis-knee-xray)**
* **[MURA v1.1 Dataset](https://www.kaggle.com/datasets/cjinny/mura-v11)**
* **[Tuberculosis (TB) Chest X-ray Dataset](https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-dataset)**
