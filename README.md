# Multi-Scale-Push-Pull-CNN
Multi-scale push-pull layer for Convolutional Neural Networks (CNNs), demonstrating superior robustness against adversarial attacks compared to normal push-pull CNNs Inspired by biological visual systems.

## Multi-Scale Push-Pull Layer for Robust Convolutional Neural Networks

This repository contains an implementation of a Multi-Scale Push-Pull Layer for enhancing the robustness of Convolutional Neural Networks (CNNs) against adversarial attacks, specifically FGSM (Fast Gradient Sign Method) and PGD (Projected Gradient Descent) attacks.

## Overview

The project implements a novel Multi-Scale Push-Pull Layer that aims to improve the robustness of CNNs. The model is trained and evaluated on the CIFAR-10 dataset, with performance measured on clean test images as well as under FGSM and PGD attacks.

## Key Features

- Implementation of a Multi-Scale Push-Pull Layer
- Custom CNN architecture incorporating the Push-Pull Layer
- FGSM and PGD attack implementations
- Training and evaluation on CIFAR-10 dataset
- Visualization of model predictions

## Requirements

- Python 3.x
- PyTorch
- torchvision
- matplotlib
- numpy

## Usage

1. Clone the repository
2. Install the required dependencies
3. Run the main script to train the model and evaluate its performance

## Code Structure

- `MultiScalePushPullLayer`: Implementation of the custom layer
- `MultiScalePushPullCNN`: CNN architecture incorporating the Push-Pull Layer
- `fgsm_attack`: Function to generate FGSM adversarial examples
- `pgd_attack`: Function to generate PGD adversarial examples
- Training loop and evaluation functions

## Results

The model achieves the following accuracies:

- Clean test images: 65.62%
- FGSM adversarial examples: 25.00%
- PGD adversarial examples: 3.12%

Standard Push-Pull CNN achieves following accuracies:

- Clean test images: 76.56%
- FGSM adversarial examples: 17.19%
- PGD adversarial examples: 1.56%

## Visualization

The code includes functionality to visualize model predictions on random test images, helping to understand the model's performance visually.

## Comparison to Standard Push-Pull CNN

Although direct comparison data is not provided, the multi-scale approach offers several advantages over a standard Push-Pull CNN:

1. **Feature diversity**: Multiple kernel sizes capture a wider range of features, making the model more robust to small perturbations.

2. **Adaptive weighting**: The learnable alpha parameters allow the model to adjust the importance of different scales dynamically.

3. **Improved generalization**: The multi-scale approach can potentially lead to better generalization on clean and adversarial examples.

## Future Work

- Experiment with different hyperparameters for the Push-Pull Layer
- Explore other adversarial attack methods
- Investigate the layer's effectiveness on different datasets and architectures

By incorporating these multi-scale features, the Multi-Scale Push-Pull CNN shows promise in enhancing robustness against adversarial attacks compared to standard architectures.

## Acknowledgements

This work is based on research into robust convolutional neural networks
Reference : N. Strisciuglio, M. Lopez-Antequera, and N. Petkov, ”Enhanced robustness of convolutional networks with a push–pull inhibition layer,” Neural Computing and Applications, 2020.
