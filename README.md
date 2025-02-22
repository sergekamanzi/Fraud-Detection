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
| Model 1               | Adam          | L2              | 100        | Yes                | 6                    |0.0003             |0.9820       |0.9698        |0.9903       |0.9502        |
| Model 2               | SDG          | L1_l2              | 100        | yes                 | 6                   | 0.001            |0.9537        |0.9261       |0.9968      |0.8648        |
| Model 3               | RMSprop       | L1           | 100      | Yes                | 6                  |0.0005           |0.9792       |0.9764       |0.9605     |0.9870       |0.9354
| Model 4               | Nadam         | L2              | 200        | Yes                | 6                   | 0.0003            |0.9905        | 0.9839       | 0.9935     | 0.9745       |
| Model 5 (default Simple NN)   | none         | None            | 10        | No                 | 3                    | 0.001             |0.8728         |0.7502       |0.6569     | 0.8745       |


### **Summary of Results**
The best-performing model in terms of accuracy, F1 score, and precision was **Model 4**, which used Nadam as the optimizer, L2 regularization, 200 epochs, early stopping, 5 layers, and a learning rate of 0.0003. This model achieved an accuracy of **0.95** and an F1 score of **0.94**, indicating that it effectively balanced precision and recall.

Here’s an updated comparison with Logistic Regression instead of XGBoost, based on the code provided:

---

**Comparison between ML Algorithm (Logistic Regression) and Neural Network**

In comparing the performance between classical machine learning (e.g., Logistic Regression) and neural network models:

The Logistic Regression model achieved solid performance, with hyperparameter tuning yielding an **accuracy** of 0.9371 and an **F1 score** of 0.8920. While this is competitive, it fell short compared to the best neural network model, which achieved higher performance on this dataset.

**Difference between Nadam + L2 and logistic regression**

Neural networks (with proper optimization techniques like early stopping, Nadam optimizer, and regularization(l2)) tend to perform better due to their ability to capture complex patterns. However, Logistic Regression is a simpler and faster model, making it a good baseline for binary classification tasks like fraud detection.

**Hyperparameters for the ML Algorithm (Logistic Regression)**
- C (Regularization strength): Tuned using GridSearchCV, best value =  10.
- Solver: Best choice =  liblinear.
- Class Weight: Balanced to handle class imbalance.

