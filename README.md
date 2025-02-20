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
| Model 1               | Adam          | L2              | 100        | Yes                | 3                    | 0.001             | 0.92         | 0.90         | 0.89       | 0.91         |
| Model 2               | Adam          | L1              | 150        | No                 | 5                    | 0.0001            | 0.85         | 0.83         | 0.82       | 0.85         |
| Model 3               | RMSprop       | None            | 50         | Yes                | 4                    | 0.001             | 0.88         | 0.86         | 0.85       | 0.87         |
| Model 4               | Nadam         | L2              | 200        | Yes                | 5                    | 0.0003            | 0.95         | 0.94         | 0.92       | 0.96         |
| Model 5 (NN Simple)   | Adam          | None            | 100        | No                 | 2                    | 0.001             | 0.80         | 0.78         | 0.77       | 0.79         |
| Model 6 (ML)          | XGBoost       | L2              | -          | -                  | -                    | -                 | 0.93         | 0.91         | 0.90       | 0.92         |

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
