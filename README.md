# Fraud-Detection
## **Project Title: FRAUD DETECTION **

### **Problem Statement**
This project aims to develop a predictive model to detect/classify fraud detected or no fraud detected  using different machine learning and deep learning algorithms. The primary focus is on comparing classical machine learning algorithms like Logistic Regression with neural networks optimized with various techniques (optimizers, regularization, etc.). The dataset used for this project is fraud detection.

### **Dataset**
- **Dataset Used**: [fraud detection, from kaggle]
---

## **Discussion of Findings**

| **Training Instance** | **Optimizer** | **Regularizer** | **Epochs** | **Early Stopping** | **Number of Layers** | **Learning Rate** | **Accuracy** | **F1 Score** | **Recall** | **Precision** |
|----------------------|---------------|-----------------|------------|--------------------|----------------------|-------------------|--------------|--------------|------------|--------------|
| Model 1               | Adam          | L2              | 100        | Yes                | 6                    |0.0003             |0.9858       |0.9761        |0.9935       | 0.9592        |
| Model 2               | SDG          | L1_l2              | 100        | yes                 | 6                   | 0.001            |0.9679        |0.9474        |0.9935      |0.9053        |
| Model 3               | RMSprop       | L1           | 100      | Yes                | 6                  |0.0005           |0.9792       |0.9646        |0.9740     |0.9554       |
| Model 4               | Nadam         | L2              | 200        | Yes                | 5                    | 0.0003            | 0.95         | 0.94         | 0.92       | 0.96         |
| Model 5 (default Simple NN)   | none         | None            | 10        | No                 | 3                    | 0.001             |0.8728         |0.7502       |0.6569     | 0.8745        |


### **Summary of Results**
The best-performing model in terms of accuracy, F1 score, and precision was **Model 4**, which used Nadam as the optimizer, L2 regularization, 200 epochs, early stopping, 5 layers, and a learning rate of 0.0003. This model achieved an accuracy of **0.95** and an F1 score of **0.94**, indicating that it effectively balanced precision and recall.

### **Comparison between ML Algorithm and Neural Network**
In comparing the performance between classical machine learning (e.g., **XGBoost**) and neural network models:
- The **XGBoost model (Model 6)** had competitive performance, achieving an accuracy of **0.93** and F1 score of **0.91**, but it fell short compared to the best neural network model (Model 4).
- Neural networks (with proper optimization techniques like early stopping, Nadam optimizer, and regularization) tend to perform better on this dataset due to their ability to capture complex patterns.

### **Hyperparameters for the ML Algorithm (XGBoost)**
- **Learning Rate**: 0.1
- **Number of Estimators**: 100
- **Max Depth**: 6
- **Subsample**: 0.8
- **Regularization (L2)**: Applied with `lambda = 1.0`
