# model-smoking-dna-methylation

This repository contains the code and data for predicting the influence of smoking on DNA methylation at different CpG islands. The
code is written in Python and uses the sklearn library for machine learning. The data is stored in csv file format and is available in
the same repository.

## Definition of the problem and initial preparation

- Question: How does smoking influence DNA methylation at different CpG islands?
- Data selection and preparation:
  - gsm, smoking status, gender, age, and DNA methylation data
- Target variable:
  - Smoking status
- Evaluation metrics:
  - Accurary
  - Precision
  - Recall
  - F1 score

## Preparation of the data

A dataset was used that includes information on smoking status, gender, age, and methulation values at specific CpG islands. The
following steps were performed for data preparation:

1. Removal of the 'GSM' column as it was not relevant for the analysis.
2. Normalization of the values in the 'Gender' column to make them uniform.
3. Imputation of missing values in the methylation columns.
4. Coding of categorial variables using LabelEncoder.
5. Normalization of methylation data using StandardScale.

## Feature selection and reduction of attributes

To improve the performance and reduction of dimensionality of dataset, attribute selection and reduction were implemented:

1. VarianceThreshold: The features with variance zero were removed.
2. SelectKBest: The top 10 features were selected.
3. PCA: THE PCA was used to reduce the dimensionality to 10 principal components.

## Training and Evaluation of the Base Model

A data split was performed to train with 80% of the data and 20% for testing. In this way, if we want to test our model, we use new
data that we have not trained with.

## Optimization of the model

The model was optimized using GridSearchCV to find the best hyperparameters for the model.

## Models used and evaluation

The following models were used for the prediction:

- Logistic Regression
- Random Forest
- SVM

The results obtained were the following:

- Logistic Regression (Base Model):

  - Accuracy: 0.74
  - Precision: 0.75
  - Recall: 0.74
  - F1 score: 0.66

- Random Forest (Advanced Model):

  - Accuracy: 0.74
  - Precision: 0.71
  - Recall: 0.74
  - F1 score: 0.70

- SVM (Advanced Model):

  - Accuracy: 0.73
  - Precision: 0.70
  - Recall: 0.73
  - F1 score: 0.66

  ### Acurracy

  We can see that all three models show similar results, with an accuracy around 74%. THis indicated that all models have comparable
  performance in terms of correctly classifying smokers and non-smokers. based on DNA methylation.

  ### Precision and F1-score

  Although the models shae accuracy, they show differences in these evaluation metrics. The Random Forest model, although it has the
  same accuracy as Logistic Regression, shows a better F1-sscore, which indicatees that it suggests a better balance between precision
  and recall.

  ### SVM

  This model has a lowe accuracy compared to the other models, Its other metrics are also lower, which indicates, in this case, that SVM is not the best model for this dataset.

  ## CONCLUSION

  It has been shown that DNA in specific CpG islands can be used to predict smoking status with reasonable accuracy using different
  models.
  It has also been shown that the Random Forest model has shown a better balance between the evaluation metrics, aking it the (slightly) best model.

  Optimiztion techniques and several models have also been used to obtain the best possible results. It should also be noted that these
  models have a lot of room for improvement.

  ## Future work

  - Use more advanced models for prediction.
  - Use more data for training.
  - Use more features for prediction.

  ## Develop by @andreeo
