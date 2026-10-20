# Artificial Neural Networks (ANN) — MNIST Classification

## Overview

This project explores Artificial Neural Networks (ANNs) using TensorFlow/Keras to classify handwritten digits and fashion images. The experiments investigate how different network architectures and activation functions affect model performance.

## Objectives

- Train a neural network to classify handwritten digits using the MNIST dataset.
- Compare ReLU and sigmoid activation functions.
- Investigate the effect of using 1, 10, and 20 hidden layers.
- Examine the effect of increasing the number of neurons in hidden layers from 16 to 128.
- Repeat the experiments using the Fashion MNIST dataset.
- Compare model performance using test accuracy and test loss.

## Datasets

**MNIST:** Contains 28 × 28 grayscale images of handwritten digits from 0 to 9.

**Fashion MNIST:** Contains 28 × 28 grayscale images representing 10 categories of clothing and footwear.

Both datasets contain 60,000 training images and 10,000 test images.

## Technologies Used

- Python
- TensorFlow and Keras
- Matplotlib
- Pandas
- Google Colab / Jupyter Notebook

## Methodology

The images are normalized by dividing pixel values by 255. The neural network uses a `Flatten` layer to convert each image into a one-dimensional vector, followed by fully connected (`Dense`) layers.

The output layer contains 10 neurons with a softmax activation function to predict one of the 10 classes.

The models are compiled using the Adam optimizer, sparse categorical cross-entropy loss, and accuracy as an evaluation metric. Each experiment uses 3 training epochs and a batch size of 5.

## Experimental Results

| Dataset | Experiment | Test Accuracy | Test Loss |
|---|---|---:|---:|
| MNIST | Original ReLU — 2 hidden layers, 16 neurons | 94.58% | 0.1911 |
| MNIST | Sigmoid — 2 hidden layers, 16 neurons | 93.54% | 0.2221 |
| MNIST | 1 hidden layer, 16 neurons | 94.53% | 0.1884 |
| MNIST | 10 hidden layers, 16 neurons | 91.93% | 0.2906 |
| MNIST | 20 hidden layers, 16 neurons | 88.46% | 0.4169 |
| MNIST | 2 hidden layers, 128 neurons | 96.05% | 0.1495 |
| Fashion MNIST | Sigmoid — 2 hidden layers, 16 neurons | 84.23% | 0.4497 |
| Fashion MNIST | 1 hidden layer, 16 neurons | 84.13% | 0.4536 |
| Fashion MNIST | 10 hidden layers, 16 neurons | 83.16% | 0.4894 |
| Fashion MNIST | 20 hidden layers, 16 neurons | 10.00% | 2.3027 |
| Fashion MNIST | 2 hidden layers, 128 neurons | 85.80% | 0.3990 |

## Key Findings

- ReLU achieved slightly higher test accuracy than sigmoid in the MNIST experiments.
- Increasing the number of hidden layers did not improve accuracy in these experiments.
- The 128-neuron architecture achieved the highest MNIST test accuracy of 96.05%.
- The Fashion MNIST model with 20 hidden layers achieved only 10% test accuracy, indicating that it did not learn the classification task effectively under the chosen training configuration.
- Fashion MNIST was more challenging than handwritten digit classification in the reported experiments.

## How to Run

1. Open the notebook `ANN_Tutorial.ipynb` in Google Colab or Jupyter Notebook.
2. Run the cells in order.
3. Ensure TensorFlow/Keras, Matplotlib, and Pandas are available in the environment.
4. Review the training output and test metrics for
