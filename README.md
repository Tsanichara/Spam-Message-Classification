# Spam Message Classification

## Project Overview

This project aims to classify messages as either spam or non-spam using machine learning techniques. The primary objective is to build models that can accurately differentiate between spam and legitimate messages, which is crucial for applications like email and SMS filtering.

## Dataset

The dataset used consists of labeled messages, with each message classified as either 'spam' or 'ham' (not spam). The data was preprocessed and balanced to ensure equal representation of both classes before being used to train the models.

### Dataset Details:
- **Total Samples**: 1,494
- **Features**: 
  - `message`: The text of the message.
  - `length`: Length of the message.
  - `punct`: Number of punctuation marks in the message.
- **Labels**: Binary labels indicating whether a message is 'spam' or 'ham'.

### Class Distribution:
- **Ham**: 86.59%
- **Spam**: 13.41%

## Project Structure

The project is structured as follows:

1. **Data Preprocessing**:
    - Loading the data and removing any missing values.
    - Balancing the dataset by undersampling the majority class (ham).
    - Visualizing the distribution of message lengths and punctuation counts for both classes.

2. **Model Building**:
    - **Random Forest**:
        - Used a pipeline with `TfidfVectorizer` for feature extraction and `RandomForestClassifier` for classification.
        - The model was trained on the preprocessed data.
    - **Support Vector Machine (SVM)**:
        - Another pipeline using `TfidfVectorizer` for feature extraction and `SVC` for classification.
        - The model was also trained on the preprocessed data.

3. **Model Evaluation**:
    - Both models were evaluated using accuracy, confusion matrix, and classification report metrics.

4. **Prediction**:
    - The final models were used to classify new messages and demonstrated the ability to distinguish between spam and ham effectively.

## Results

### Random Forest:
- **Accuracy**: 95.10%
- **Confusion Matrix**:
  - True Negatives: 224
  - False Positives: 3
  - False Negatives: 19
  - True Positives: 203
- **Classification Report**:
  - **Ham**:
    - Precision: 0.92
    - Recall: 0.99
    - F1-Score: 0.95
  - **Spam**:
    - Precision: 0.99
    - Recall: 0.91
    - F1-Score: 0.95

### Support Vector Machine (SVM):
- **Accuracy**: 94.88%
- **Confusion Matrix**:
  - True Negatives: 222
  - False Positives: 5
  - False Negatives: 18
  - True Positives: 204
- **Classification Report**:
  - **Ham**:
    - Precision: 0.93
    - Recall: 0.98
    - F1-Score: 0.95
  - **Spam**:
    - Precision: 0.98
    - Recall: 0.92
    - F1-Score: 0.95

These results show that both models perform well in classifying spam messages, with Random Forest achieving slightly better accuracy.

## Conclusion

This project demonstrates the effective use of machine learning techniques for classifying spam messages. The models developed can be applied to various communication platforms for spam filtering, significantly enhancing the user experience by reducing unwanted messages.
