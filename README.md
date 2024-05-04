# Tomato Disease Classification with Deep Learning

# My Choice of Assignment:

- For this assignment, I have decided to dive into the Training Option - OPTION 1,
  where I got to play around with PyTorch and really put it through its paces.
- My adventure began with a fascinating dataset I found on Kaggle, all about
  tomato plant diseases.
- It's not just any dataset; this one's special because it has over 5000 images that
  really tested the mettle of my models. I ended up training two different types of
  models to see how they'd perform.
- Along the way, I also tinkered with some models from Torchvision, tweaking them
  here and there to better suit my needs.
- All of this was done using PyTorch 1.6 or newer, sticking to the guidelines but
  also pushing the boundaries.
- The results? Well, they're visually summed up in comparisons that show just how
  far we've come in making machines understand what they're seeing.
- It's been quite the journey, and I'm excited to share the leaps I've made in image
  classification.

## Github Link:

- https://github.com/hpuppala26/CMPE_258_Assignment_02

## Overview

This project applies modern deep learning techniques to classify and diagnose diseases in tomato plants. Utilizing the publicly available "Tomato Diseases" dataset from Kaggle, this repository contains the implementation of various models including ResNet, AlexNet, and VGG, each tailored to recognize different diseases affecting tomato plants.

## Dataset

The dataset is sourced from [Kaggle's Tomato Diseases dataset](https://www.kaggle.com/datasets/luisolazo/tomato-diseases). It includes over 5,000 images across five categories, labeled and ready for training robust deep learning models.

- **Format**: JPEG
- **Resolution**: Variable
- **Quantity**: 5,000 images
- **Categories**: Bacterial spot, Late blight, Leaf mold, Yellow leaf curl virus, Healthy

## Prerequisites

- PyTorch 1.6 or newer
- Torchvision
- Python 3.6 or above

## Installation

To set up the environment for this project, run the following commands:

```bash
pip install torch torchvision
```

## Models and Configuration

### Model 1: ResNet

- **Optimizer**: SGD
- **Learning Rate Scheduler**: StepLR
- **Momentum**: 0.9
- **Learning Rate**: 0.1
- **Epochs**: 40

- **Inferences**:
  After training a model using a ResNet architecture with an initial learning rate of 0.1, employing
  an SGD optimizer and a momentum of 0.9, and adjusting the learning rate with StepLR, the
  results are in—and they're pretty impressive. The model achieved high validation accuracy,
  peaking at 96.69%, and showed great promise in distinguishing between various conditions
  affecting tomato plants. The most notable successes were in identifying bacterial spots, with a
  97% test accuracy, and late blight, with a 98% test accuracy. This high level of performance
  suggests that the model has effectively learned to discern the intricate patterns of disease from
  healthy plant conditions. It's a strong start, and with a little more tuning, we might just be on the
  cusp of something that could significantly aid farmers in early disease detection.

### Model 2: AlexNet

- **Optimizer**: Adam
- **Learning Rate Scheduler**: StepLR
- **Momentum**: 0.9
- **Learning Rate**: 0.1
- **Epochs**: 20

- **Inferences**:
  Leveraging the AlexNet architecture, my model was configured with an Adam optimizer,
  using a momentum of 0.9 and an initial learning rate of 0.1 managed by a StepLR
  learning rate scheduler. The results were compelling, with the model demonstrating
  exceptional proficiency across the board. Notably, it achieved a remarkable overall test
  accuracy exceeding 99%, indicative of its capability to discern with high precision the
  health conditions of tomato plants. These outcomes underscore the model’s potential
  as a tool for accurate plant disease diagnosis in agricultural practices.

### Model 3: VGG

- **Optimizer**: Adam
- **Learning Rate Scheduler**: OneCycleLR
- **Momentum**: 0.9
- **Learning Rate**: 0.1
- **Epochs**: 20

- **Inferences**:
  In this segment, the VGG model took an important step. Configured with the Adam optimizer
  and a robust momentum of 0.9, it was trained over 20 epochs using a OneCycleLR learning
  rate policy starting at 0.1. The precision of this model was on full display, with each epoch
  bringing us closer to our goal. The final act was a demonstration of stellar performance, with test
  accuracies reaching into the high 90s for each category, and an overall accuracy of 92%, a
  testament to the model's capability to decode the complexities of plant health. This thing
  strengthened my understanding of image classification.
