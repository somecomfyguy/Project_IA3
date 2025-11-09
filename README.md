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

- Analyze the vulnerability of **YOLO** object detection models to adversarial attacks.
- Implement and evaluate two attack methods: **PGD** and **DeepFool**.
- Implement and assess defense strategies: **Adversarial Training** and **Jacobian Regularization**.
- Compare model performance on clean and adversarially perturbed data.

---

## Dataset

We use the **COCO dataset** (Common Objects in Context):

- Large-scale object detection, segmentation, and captioning dataset.
- 80 object categories.
- Contains over 200,000 labeled images.
- Standard preprocessing: resizing, normalization, and data augmentation.

### Defenses

#### Adversarial Training

- Augments training data with adversarial examples.
- YOLO model learns to correctly detect objects in both clean and adversarial images.
- Improves robustness against attacks seen during training.

#### Jacobian Regularization

- Adds a regularization term to the loss function based on the Jacobian of the model’s output w.r.t input.
- Encourages smoother model gradients, making YOLO less sensitive to small perturbations.

---
