# Comparing Neural Network Implementations: Keras Sequential, Keras Functional API, and PyTorch on MNIST

This repository contains a comparison of three different neural network implementation paradigms using the MNIST dataset. The goal is to highlight the similarities and differences between:

1. **Keras Sequential Model**
2. **Keras Functional API**
3. **PyTorch Modular Implementation**

By training the same neural network architecture across these three approaches, this project serves as a practical reference for beginners and developers who want to understand how these frameworks and APIs differ in practice.

## Overview

### What is MNIST?
The [MNIST dataset](http://yann.lecun.com/exdb/mnist/) is a classic machine learning benchmark consisting of 70,000 grayscale images of handwritten digits (0-9). Each image is 28x28 pixels. It is widely used for testing and comparing machine learning models due to its simplicity and accessibility.

### Why Compare Different Frameworks and Approaches?
Each framework offers a unique style for defining and training models:

- **Keras Sequential API**:  
  A simple and linear approach to model building, ideal for straightforward architectures.
  
- **Keras Functional API**:  
  A flexible API for defining models with shared layers, branching, or multiple inputs/outputs.
  
- **PyTorch Implementation**:  
  A lower-level, dynamic computation framework that offers explicit control over the model definition and training process.

This comparison helps users appreciate the differences in syntax, design philosophy, and usability between these approaches.

## Repository Structure

- **`mnist_framework_comparison.ipynb`**:  
  A single Jupyter notebook that implements all three approaches to building and training a neural network on the MNIST dataset. Each section of the notebook focuses on one of the three methods, providing a consistent structure for easy comparison.

## Neural Network Details

All three models use the **same neural network architecture**, training process, and evaluation setup to ensure a fair comparison:

- **Architecture**:
  - Input Layer: 784 neurons (flattened from the 28x28 images)
  - Hidden Layer: Dense layer with 128 neurons and ReLU activation
  - Output Layer: Dense layer with 10 neurons (softmax activation for multi-class classification)
  
- **Compilation**:
  - Optimizer: Adam (learning rate = 0.001)
  - Loss Function: Categorical Crossentropy
  - Metrics: Accuracy
  
- **Training**:
  - Batch size: 32
  - Epochs: 15

## Results and Insights

| Framework/API       | Test Accuracy |  
|----------------------|---------------|  
| Keras Sequential     | 96.43%        |  
| Keras Functional API | 97.41%        |  
| PyTorch              | 97.46%        |  

### Note:
The accuracy differences between the three approaches are minor and likely due to randomness (e.g., weight initialization and data shuffling) as no seed was set during training. Setting a seed would likely yield consistent results across all three methods.

### Observations:
- All three implementations performed exceptionally well on the MNIST dataset, demonstrating that model design and training methodology are more critical than the choice of framework.
- The slight variations in test accuracy are statistically insignificant without a controlled seed.

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Ahmed-Alqershi/deep_learning_framework_comparison.git
   cd deep_learning_framework_comparison
   ```

2. Install dependencies:
   ```bash
    pip install -r requirements.txt
   ```
     This installs TensorFlow (for Keras), PyTorch, and other essential packages.

3. Run the notebook:
   ```bash
    jupyter notebook mnist_framework_comparison.ipynb
   ```
     Open the notebook in your browser and follow the sections to explore how each framework is used.

## Key Takeaways

- The **Keras Sequential API** provides a straightforward and beginner-friendly approach for building models, ideal for simple, linear architectures.
- The **Keras Functional API** adds flexibility for creating more complex architectures, such as models with shared layers, branching, or multiple inputs and outputs.
- **PyTorch** offers low-level, dynamic control over model definition and training, making it a preferred choice for research and experimental work.

Despite their differences in implementation style, all three frameworks delivered excellent results on the MNIST dataset, demonstrating that the choice of framework often depends on the user's needs and preferences.

## Contributing

Contributions are welcome! If you have suggestions for improvements or encounter any issues:

1. Fork the repository.
2. Make your changes.
3. Submit a pull request with a detailed description of your updates.

## License

This project is licensed under the [MIT License](https://opensource.org/license/mit). You are free to use, modify, and distribute this code as per the license terms.

---

This repository is intended to help users understand and compare the Keras Sequential API, Keras Functional API, and PyTorch implementation styles for building neural networks. I hope it serves as a valuable resource for your learning journey!

