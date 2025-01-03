# Evasion Attacks against Machine Learning Models

This project demonstrates how to perform evasion attacks against Machine Learning (ML) models using the SecML library in Python.

## Introduction

Evasion attacks are a type of adversarial attack where an attacker tries to perturb input data to cause a machine learning model to misclassify it. These attacks can have serious consequences in real-world applications, such as autonomous driving, facial recognition, and spam filtering.

This project explores evasion attacks against two types of ML models: Support Vector Machines (SVMs) and Neural Networks. We use the SecML library to implement the attacks and evaluate their effectiveness.

## Project Structure

The project is organized as follows:

1. **Data Loading and Preprocessing:** Loads a synthetic dataset using `CDLRandomBlobs` from SecML, splits the data into training and testing sets, and normalizes the data using `CNormalizerMinMax`.

2. **Model Training:** Creates an SVM classifier with an RBF kernel using `CClassifierSVM`, trains the classifier on the training data using `clf1.fit()`, and evaluates the accuracy of the classifier on the test data using `CMetricAccuracy`.

3. **Evasion Attack:** Performs an evasion attack using `CFoolboxPGDL2` from SecML's adversarial module. Defines attack parameters such as maximum perturbation (`eps`), step size (`alpha`), and number of iterations (`steps`). Executes the attack using `pgd_attack.run()`.

4. **Visualization:** Visualizes the attack by plotting the decision regions, the adversarial example, and the constraint region.

5. **MNIST Classification and Attack:** Loads the MNIST dataset, defines a neural network using PyTorch, trains the network using SecML's `CClassifierPyTorch` wrapper, evaluates the accuracy of the network on the test data, performs a similar evasion attack using `CFoolboxPGDLinf`, and performs security evaluation using `CSecEval` to analyze the attack's effectiveness.

## Requirements

- Python 3.6 or higher
- SecML library
- PyTorch library
- Matplotlib library

## License
This project is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License. See the [LICENSE](./LICENSE) file for details.
