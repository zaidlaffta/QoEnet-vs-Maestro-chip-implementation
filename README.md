QoEnet vs Maestro, Lightweight C Implementation for Embedded Wi Fi QoE Prediction

This repository contains a minimal C implementation of two Quality of Experience prediction approaches for Wi Fi networks, QoEnet and Maestro. The goal of this project is to compare the computational complexity, memory footprint, and inference characteristics of a tree based model versus a recurrent neural network model when deployed in resource constrained environments such as wireless access points, embedded devices, or edge networking platforms.

QoEnet is implemented as a Random Forest style predictor composed of lightweight decision trees. Each tree performs a series of simple threshold comparisons on Wi Fi control features, including channel width, PHY mode, access category, and airtime fairness, and outputs a predicted QoE score. The final prediction is obtained by averaging the outputs across all trees in the ensemble. Because the model relies only on conditional comparisons and arithmetic operations, it is well suited for embedded deployment in firmware or low power networking devices.

Maestro is implemented as a simplified Long Short Term Memory network following the structure described in the Maestro research paper. The model maintains hidden and cell states and performs recurrent computations using sigmoid and tanh activation functions. This implementation is included to illustrate the increased computational and memory requirements of recurrent neural models compared to tree based approaches when targeting embedded platforms.

The purpose of this repository is to provide a transparent comparison between the two architectures from a systems perspective. In addition to prediction accuracy, the project evaluates code size, runtime latency, and implementation complexity in C, which is representative of what would be required for deployment in networking firmware or embedded control processors.

This repository is intended for researchers and engineers interested in applying machine learning to wireless networking systems, particularly in environments where computational efficiency and deployability on embedded hardware are critical considerations.

Key Features

Lightweight C implementation of QoEnet Random Forest inference
Simplified C implementation of Maestro LSTM inference
Direct comparison of model structure, complexity, and runtime behavior
Designed for portability to embedded platforms such as ARM based networking SoCs or microcontrollers
Suitable for experimentation with firmware level QoE prediction

Typical Use Cases

Embedded Wi Fi access point firmware
Edge networking devices and routers
Research on deployable ML models for networking systems
Performance comparisons between tree based and neural QoE predictors

License

This code is provided for research and educational purposes. You comercialize it and I will come after you. Thank you. 
