# Object Recognition: Attacks and Defenses

## Table of Contents

- [Introduction](#introduction)
- [Project Objectives](#project-objectives)
- [Dataset](#dataset)
- [Methods](#methods)
  - [Object Recognition Models](#object-recognition-models)
  - [Adversarial Attacks](#adversarial-attacks)
    - [Projected Gradient Descent (PGD)](#projected-gradient-descent-pgd)
    - [DeepFool](#deepfool)
  - [Defenses](#defenses)
    - [Adversarial Training](#adversarial-training)
    - [Jacobian Regularization](#jacobian-regularization)
- [Implementation](#implementation)
- [Results](#results)
- [References](#references)

---

## Introduction

Deep learning models for object recognition have achieved remarkable accuracy but are vulnerable to **adversarial attacks**, where small perturbations to input images can lead to misclassification or missed detections. This project investigates common attack methods and evaluates defense mechanisms to improve the robustness of object detection systems.

---

## Project Objectives
- Implement a model for object detection
- Implement and evaluate two attack methods: **PGD** and **DeepFool**.
- Implement and assess defense strategies: **Adversarial Training** and **Jacobian Regularization**.
- Compare model performance on clean and adversarially perturbed data.

---
## Adversarial Attacks
### Projected Gradient Descent (PGD)

- Iterative adversarial attack that refines perturbations over multiple steps.
- At each iteration, the input is modified in the direction of the gradient of the loss w.r.t. the input.
- The perturbation is projected back into a valid range (bounded by a norm constraint, typically L_{inf}).
- Known for being one of the strongest first-order attacks and widely used to test model robustness.

### DeepFool

- Iterative attack that finds the minimal perturbation required to change a model’s classification.
- Approximates the decision boundary locally as a hyperplane and moves the input across it.
- Generates small, human imperceptible perturbations.
- Useful for evaluating a model’s sensitivity to small, precise changes in input.

## Dataset

We use the **CIFAT-10** dataset

- 60000 32x32x3 (color) images
- 10 classes
- 6000 pictures for each class
- There are 50000 training images and 10000 test images

## Defenses

### Adversarial Training

- Augments training data with adversarial examples.
- Improves robustness against attacks seen during training.

### Jacobian Regularization

- Adds a regularization term to the loss function based on the Jacobian of the model’s output w.r.t input.
- Encourages smoother model gradients

---
### References

https://www.cs.toronto.edu/~kriz/cifar.html

---
