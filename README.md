# Multi-layer Perceptron (MLP) Visualization

This repository contains Python code for creating and visualizing Multi-layer Perceptrons (MLPs) with varying numbers of hidden layers. The code demonstrates how the decision boundaries of an MLP change with the complexity of the network, specifically using the XOR problem as a classification task.

## Table of Contents

1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Installation](#installation)
4. [Usage](#usage)
5. [How It Works](#how-it-works)
6. [Examples](#examples)
7. [Results](#results)
8. [Troubleshooting](#troubleshooting)
9. [FAQs](#faqs)
10. [License](#license)

## Overview

This project showcases how to build and visualize Multi-layer Perceptrons (MLPs) for solving the XOR classification problem. It demonstrates the impact of adding hidden layers on the model's ability to learn and separate the classes in a non-linearly separable problem.

## Requirements

To run the code, you'll need the following Python libraries:

- `numpy`
- `matplotlib`
- `tensorflow`

You can install these libraries using pip:

```bash
pip install numpy matplotlib tensorflow
```

## Installation

1. **Clone the Repository**:

    ```bash
    git clone https://github.com/yourusername/mlp-visualization.git
    ```

2. **Navigate to the Project Directory**:

    ```bash
    cd mlp-visualization
    ```

3. **Install Required Libraries**:

    ```bash
    pip install numpy matplotlib tensorflow
    ```

## Usage

1. **Run the Python Script**:

    Execute the script to create and visualize the MLP models:

    ```bash
    python mlp_visualization.py
    ```

2. **View the Output**:

    The script will display plots showing the decision boundaries for MLP models with different numbers of hidden layers (0, 1, and 2).

## How It Works

### Data Generation
Synthetic XOR data is used for binary classification.
- **Dataset**: The XOR problem is used as a binary classification task with four data points:
  - Inputs: `[[0, 0], [0, 1], [1, 0], [1, 1]]`
  - Targets: `[0, 1, 1, 0]`

### Model Creation

- **Function**: `create_and_train_model(hidden_layers)`
  - **Architecture**: Creates an MLP with the specified number of hidden layers. Each hidden layer has 10 neurons and uses the ReLU activation function.
  - **Compilation**: The model is compiled with the Adam optimizer and binary cross-entropy loss function.
  - **Training**: Trained for 1000 epochs on the XOR data.

### Decision Boundary Visualization

- **Function**: `plot_decision_boundary(model, title)`
  - **Grid Creation**: Generates a grid of points covering the feature space.
  - **Prediction**: Uses the trained model to predict probabilities for each grid point.
  - **Plotting**: Plots the decision boundary along with the data points. The decision boundary is shown as a contour plot, and the data points are overlaid with colors representing their class labels.

### Model Training and Visualization

- **Process**:
  - Models with 0, 1, and 2 hidden layers are created and trained.
  - The decision boundaries for these models are plotted to illustrate how additional hidden layers affect the model's ability to separate the XOR classes.

## Examples

### Basic Execution

To run the script and visualize the MLP models:

```bash
python mlp_visualization.py
```

### Customization

You can modify the following parameters in the script to explore different scenarios:
- **Number of Hidden Layers**: Adjust the hidden layers in the `create_and_train_model` function.
- **Number of Epochs**: Change the number of epochs for training.

## Results

The script generates three plots with decision boundaries for MLP models with:
- **0 Hidden Layers**: Displays a linear boundary (perceptron), which is not sufficient to solve the XOR problem.
- **1 Hidden Layer**: Shows a non-linear boundary that can separate the XOR classes.
- **2 Hidden Layers**: Further refines the decision boundary, demonstrating improved separation capabilities.

The plots illustrate the effect of increasing model complexity on the ability to solve non-linearly separable problems.

**Multi Layer Perceptron with 0 hidden layer:**
![Multi Layer Perceptron with 0 hidden layer](https://github.com/AartiDashore/MultiLayerPerceptron/blob/main/MLP_0.png)

**Multi Layer Perceptron with 1 hidden layer:**
![Multi Layer Perceptron with 1 hidden layer](https://github.com/AartiDashore/MultiLayerPerceptron/blob/main/MLP_1.png)

**Multi Layer Perceptron with 2 hidden layer:**
![Multi Layer Perceptron with 2 hidden layer](https://github.com/AartiDashore/MultiLayerPerceptron/blob/main/MLP_2.png)

## Troubleshooting

### Common Issues

1. **Module Not Found Error**:
    - Ensure all required libraries are installed.
    - Check your Python environment.

2. **Plot Not Displaying**:
    - Ensure that `matplotlib` is installed and configured correctly.
    - Try running the script in an environment that supports plotting, such as Jupyter Notebook or a local IDE.

## FAQs

### What is an MLP?

A Multi-layer Perceptron (MLP) is a type of neural network with one or more hidden layers between the input and output layers. It is used for solving complex classification and regression tasks.

### How does adding hidden layers affect the MLP?

Adding hidden layers increases the model's ability to learn complex patterns and non-linear relationships in the data. It can improve the model's performance on tasks like the XOR problem.

### What is the XOR problem?

The XOR problem is a classic example in machine learning used to demonstrate the need for non-linear models. It involves classifying data points that are not linearly separable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
