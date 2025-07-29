# EEG Signal Classification using Hybrid CNN-LSTM Model

This project implements a deep learning model for classifying EEG signals into 5 different categories using a hybrid architecture combining Convolutional Neural Networks (CNN) and Long Short-Term Memory (LSTM) networks.

## Table of Contents
- [Project Description](#project-description)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Description
The goal of this project is to classify EEG signals into 5 distinct categories using advanced deep learning techniques. The model combines:
- 2D Convolutional layers for spatial feature extraction
- LSTM layers for temporal sequence modeling
- Dense layers for final classification

The implementation includes data preprocessing, class balancing with SMOTE, and performance evaluation using F1-score.

## Dataset
The dataset consists of EEG signals stored in `.npy` files, organized in folders labeled 0-4 representing different classes. Each sample has dimensions of 51×59 (time steps × channels).

## Model Architecture
The hybrid CNN-LSTM model consists of:
1. Two Conv2D layers with BatchNormalization and MaxPooling
2. Reshape layer to prepare for LSTM
3. Two LSTM layers (128 and 64 units)
4. Three Dense layers (512, 256, and 5 units) with Dropout

## Features
- Data normalization using StandardScaler
- Class imbalance handling with SMOTE
- Learning rate scheduling
- F1-score tracking during training
- Comprehensive visualization of training metrics

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/eeg-classification.git
   cd eeg-classification
