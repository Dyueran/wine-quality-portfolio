# Red Wine Quality Classification

Data science portfolio project. The aim is to find out whether the physicochemical properties of red wine can be used to classify wines into two quality groups, "good" (quality 6 or above) and "average" (quality 5 or below). This cut-off is a rule I chose for this project, not an official definition.

## Results

Test accuracy on the same 272 test wines, and the mean of 5-fold cross-validation on all 1359 wines:

| model | test accuracy | 5-fold CV mean |
|---|---|---|
| Logistic Regression | 0.735 | 0.730 |
| Naive Bayes | 0.724 | 0.720 |
| Decision Tree | 0.625 | 0.648 |
| Random Forest | 0.750 | 0.723 |

Logistic Regression, Naive Bayes and Random Forest are very close in cross-validation, so I cannot say that one is really better. The Decision Tree overfitted the training data and was the weakest.

As a secondary analysis, Linear Regression predicted the quality score with an RMSE of 0.703 and an R² of 0.384 on the test set.

## Files

- `wine_quality_draft.ipynb`: the notebook with the explanations, code and results
- `winequality-red.csv`: the red wine data

## Data

The data is the red wine file from the Wine Quality dataset on the UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/186/wine+quality

It was collected by Cortez et al. (2009), "Modeling wine preferences by data mining from physicochemical properties", Decision Support Systems 47(4), and is licensed under CC BY 4.0. I did not change any of the values.

## How to run

1. Install Python and the libraries pandas, scikit-learn and matplotlib.
2. Put `wine_quality_draft.ipynb` and `winequality-red.csv` in the same folder.
3. Open the notebook in Jupyter and run all cells.
