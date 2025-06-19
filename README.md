# Loan Prediction Model – Analytics Vidhya Competition

This repository contains my solution for the **Analytics Vidhya Loan Prediction** competition. The challenge involved building a machine learning model to predict loan approval status based on various applicant features.

## Competition Overview

Participants were provided with two datasets:

* `train.csv`: Contains labeled data including the target column `Loan_Status`.
* `test.csv`: Contains unlabeled data used to generate final predictions.

The objective was to train a predictive model on the training data and use it to make predictions on the test set. Submitted predictions were evaluated on the Analytics Vidhya platform based on accuracy, and rankings were assigned accordingly.

## Approach

1. Performed data preprocessing and exploration on the training dataset.
2. Trained and evaluated multiple classification models:

   * Decision Tree
   * Random Forest
   * Logistic Regression
   * Naive Bayes
3. Used `train_test_split` on the training data to evaluate models before final submission.
4. Applied hyperparameter tuning using `GridSearchCV` to optimize model performance.
5. Generated predictions on the test data for submission.

## Model Performance

| Model               | Local Accuracy | Submission Accuracy | Remarks              |
| ------------------- | -------------- | ------------------- | -------------------- |
| Random Forest       | 91%            | 73%                 | Overfitting occurred |
| Logistic Regression | Around 77%     | 77%                 | Final chosen model   |

At one point, the Random Forest model gave a high local accuracy of 91%, but the score dropped significantly upon submission, indicating overfitting. After rebuilding the models and tuning parameters, Logistic Regression provided a more generalizable performance with a final accuracy of 77%.

## Results

* **Final Model Used**: Logistic Regression with hyperparameter tuning
* **Final Submission Accuracy**: 77%
* **Analytics Vidhya Rank**: 8231

## Files Included

* `train.csv`: Training dataset
* `test.csv`: Test dataset
* `loan_prediction.ipynb`: Complete model training and evaluation notebook
* `submission.csv`: Final prediction file submitted

## Conclusion

This competition helped reinforce key concepts in classification, model selection, overfitting, and hyperparameter tuning. It also provided practical experience in participating in a real-world machine learning competition.

