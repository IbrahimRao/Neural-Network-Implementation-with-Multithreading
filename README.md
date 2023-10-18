# Neural-Network-Implementation-with-Multithreading

This repository contains a C++ program that implements a neural network using multithreading, inter-process communication, and synchronization techniques. The program is designed to perform forward and backward propagation calculations in a neural network and print the output. This README provides an overview of the code structure and its functionality.

# Overview
Neural networks are a fundamental part of machine learning and artificial intelligence. This code is an educational project that demonstrates the basic mechanics of a neural network, focusing on forward and backward propagation through hidden layers. It uses multithreading for parallel processing and inter-process communication to pass information between layers. The code is designed to be instructional and may require further refinement for production use.

# Prerequisites
Before you can run this code, you need the following prerequisites:

- C++ Compiler: You should have a C++ compiler (e.g., g++) installed on your machine.
- pthread: The program uses the pthread library for multithreading. Make sure it's available on your system.
- SFML: Some parts of the code refer to the SFML library (Simple and Fast Multimedia Library), although the code does not appear to use SFML directly. Install it from the official website if needed.

# Code Structure
The code is organized as follows:

- It includes essential C++ libraries, structures, and classes for managing the neural network and synchronization.
- Function prototypes are defined at the beginning of the code.
- The main function initializes the neural network and creates a child process to begin the neural network processing.
- Several functions (ImplementInputFunctionality, HiddenLayerProcessing, ImplementLayerFunctionality, and ImplementOutputFunctionality) are responsible for handling input, hidden layers, and output processing.

# How It Works

1. The program starts by creating a child process for neural network processing.
2. The input layer is set up, and threads are created for each input neuron.
3. Each thread reads input values from a configuration file, calculates weights, and performs simple matrix multiplication.
4. Threads run in parallel, handling calculations for one input neuron.
5. Synchronization ensures that all threads complete their work before proceeding.
6. Pipes are created for inter-process communication.
7. Hidden layers are processed, and more child processes are created for further layers.
8. Backpropagation calculations are performed within the code.
9. Output processing calculates Fx(X1) and prints the result.
