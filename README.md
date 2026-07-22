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
