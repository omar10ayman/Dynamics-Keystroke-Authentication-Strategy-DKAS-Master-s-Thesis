# Keystroke Dynamics Authentication using CNN1D (Model 1)

## Overview
This project presents a deep learning approach for user authentication based on **Keystroke Dynamics**, a behavioral biometric technique that identifies users through their typing patterns. The model is trained on the **CMU Keystroke Dynamics Benchmark Dataset** and performs multiclass user identification using a one-dimensional Convolutional Neural Network (CNN1D).

## Features
- Data preprocessing and cleaning
- Feature scaling using StandardScaler
- Correlation-based feature selection
- Label encoding for user identities
- CNN1D architecture for multiclass classification
- Model training with validation monitoring
- Performance evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC Curve
  - Confusion Matrix
- Authentication simulation for genuine and impostor users
- Security metrics including:
  - False Acceptance Rate (FAR)
  - False Rejection Rate (FRR)
  - Equal Error Rate (EER)
- SHAP explainability for feature importance analysis

## Dataset
- **Dataset:** CMU Keystroke Dynamics Benchmark Dataset
- Behavioral biometric data collected from users typing the same password multiple times.
- Target variable: **Subject ID**

## Project Workflow

1. Load the dataset
2. Data preprocessing
3. Feature scaling
4. Feature selection
5. Train/Validation/Test split
6. Build CNN1D model
7. Train the model
8. Evaluate performance
9. Perform authentication testing
10. Explain predictions using SHAP

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Seaborn
- SHAP

## Model Evaluation

The notebook evaluates the model using several biometric and classification metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC Curve
- Confusion Matrix
- FAR (False Acceptance Rate)
- FRR (False Rejection Rate)
- EER (Equal Error Rate)
## Experimental Results

The proposed CNN1D-based keystroke dynamics authentication framework demonstrates strong performance on the CMU Keystroke Dynamics Benchmark Dataset.

### Performance Metrics

| Metric | Value |
|--------|-------:|
| Test Accuracy | **95.00%** |
| False Acceptance Rate (FAR) | **0.03%** |
| False Rejection Rate (FRR) | **10.16%** |
| Equal Error Rate (EER) | **1.02%** |
| Decision Threshold | **0.90** |
| Precision (per enrolled user) | **> 90%** |

Experimental results demonstrate that the proposed framework achieves a **95% test accuracy**, with a **False Acceptance Rate (FAR) of 0.03%**, a **False Rejection Rate (FRR) of 10.16%** at a decision threshold of **0.90**, and an **Equal Error Rate (EER) of 1.02%**. Furthermore, the model attains **precision exceeding 90% for every enrolled user**, highlighting its strong capability to accurately distinguish genuine users from impostors while maintaining a low false acceptance rate.
## Explainability

To improve model transparency, SHAP is used to identify the most influential keystroke features contributing to authentication decisions.

## Future Improvements

- Experiment with ResNet1D and Transformer-based models.
- Apply data augmentation techniques.
- Hyperparameter optimization.
- Cross-dataset evaluation.
- Real-time authentication deployment.

## License

This project is intended for research and educational purposes.

# Keystroke Dynamics Authentication using Resnet1D (Model 2)


Keystroke dynamics has emerged as a reliable behavioral biometric for user authentication due to its non-intrusive nature, low deployment cost, and ability to capture unique typing patterns. This project presents an end-to-end deep learning framework for fixed-text keystroke dynamics authentication using the **CMU Keystroke Dynamics Benchmark Dataset**. The framework is designed to learn discriminative temporal representations directly from keystroke timing features while achieving high authentication accuracy and robust generalization.

The proposed architecture combines a **ResNet1D** backbone with **Bidirectional Long Short-Term Memory (BiLSTM)** and an **Attention Pooling** mechanism. ResNet1D extracts hierarchical local temporal features from keystroke sequences through residual learning, while the BiLSTM captures long-range contextual dependencies in both forward and backward directions. The attention pooling layer automatically assigns higher importance to the most informative temporal features, enabling the model to focus on keystroke events that contribute most significantly to user identification.

To improve model robustness and reduce overfitting, several optimization strategies are incorporated throughout the training process. These include **StandardScaler** normalization, Gaussian noise augmentation, **Mixup** data augmentation, **Label Smoothing**, **Cosine Annealing Learning Rate Scheduling**, gradient clipping, dropout regularization, and **Early Stopping** based on validation loss. Together, these techniques enhance class separability, improve convergence, and increase the model's ability to generalize to unseen samples.

The proposed framework is evaluated using a comprehensive set of biometric and classification metrics, including **Accuracy, Precision, Recall, F1-Score, ROC Curve, Confusion Matrix, False Acceptance Rate (FAR), False Rejection Rate (FRR),** and **Equal Error Rate (EER)**. Authentication performance is further analyzed using genuine and impostor verification scenarios to assess the practical reliability of the system in real-world biometric applications.

Experimental results demonstrate that the proposed framework achieves a **95% test accuracy**, with a **False Acceptance Rate (FAR) of 0.03%**, a **False Rejection Rate (FRR) of 10.16%** at a decision threshold of **0.90**, and an **Equal Error Rate (EER) of 1.02%**. Furthermore, the model attains **precision exceeding 90% for every enrolled user**, indicating its strong capability to accurately distinguish genuine users from impostors while maintaining a very low false acceptance rate.

Overall, this project demonstrates that integrating **ResNet1D**, **BiLSTM**, and **Attention Pooling**, together with modern deep learning optimization techniques such as Mixup and Label Smoothing, provides an accurate, robust, and scalable solution for keystroke-based biometric authentication. The implementation can serve as a strong baseline for future research in behavioral biometrics and explainable deep learning.
