# Credit Card Fraud Detection using Random Forest Classifier implemented from Scratch

## Overview

This project aims to detect fraudulent credit card transactions using a custom implementation of a Random Forest classifier. The dataset used is highly imbalanced, so a balanced subsample was created to improve model performance.

## Dataset

The dataset used in this project is a collection of credit card transactions with the following key features:

- **Time**: The time elapsed between this transaction and the first transaction in the dataset.
- **Amount**: The transaction amount.
- **Class**: The target variable, where `1` indicates a fraudulent transaction and `0` indicates a non-fraudulent transaction.

## Preprocessing

To handle the class imbalance, a subsample was created where the ratio of fraud to non-fraud cases is 50/50. Additionally, the `Time` and `Amount` features were scaled using `StandardScaler`.

## Model Implementation

### Custom Random Forest Classifier

A Random Forest classifier was implemented from scratch, which involved the following steps:

1. **Decision Tree Implementation**: The foundation of the Random Forest was built using a custom decision tree implementation.
2. **Random Forest Construction**: Multiple decision trees were trained on bootstrap samples, and the final prediction was made based on the majority vote from all trees.

### Key Features:

- **Bootstrap Sampling**: Each tree in the forest was trained on a random sample of the data.
- **Information Gain**: The best split for each node was determined using information gain.
- **Entropy Calculation**: Entropy was used to measure the purity of the splits.

## Evaluation

The model was evaluated on a test set using several metrics:

- **Accuracy**: The percentage of correct predictions made by the model.
- **Precision**: The proportion of positive predictions that were actually correct.
- **Recall**: The proportion of actual positive cases that were correctly identified by the model.
- **F1 Score**: The harmonic mean of precision and recall, providing a balance between the two.

The model demonstrated satisfactory performance, effectively distinguishing between fraudulent and non-fraudulent transactions.

## Results

- **Balanced Dataset**: The model was trained on a balanced dataset with a 50/50 fraud-to-non-fraud ratio.
- **Confusion Matrix**: The confusion matrix provided insights into the number of true positives, true negatives, false positives, and false negatives.

## Conclusion

This project highlights the importance of data preprocessing in dealing with imbalanced datasets. The custom Random Forest classifier performed well on the balanced subsample, providing accurate predictions for both classes. Future work could involve further optimizing the model and getting high accuracy afetr applying it to the original imbalanced dataset.

# Acknowledgements
This project was inspired by the need to address class imbalance in fraud detection. The dataset used is available from Kaggle.
