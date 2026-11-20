# Breast Cancer Diagnosis Classifier

Classifies breast tumours as **benign** or **malignant** from 30 measurements of cell nuclei, using the Breast Cancer Wisconsin (Diagnostic) dataset (569 cases).

## Results

| Model | Features | Test accuracy | False negatives (of 171 test cases) |
|---|---|---|---|
| Logistic Regression | all 30 | **96.5%** | 5 |
| Random Forest | all 30 | 95.3% | 7 |
| Logistic Regression | 5 most correlated | 92.4% | more than double |

The best model reached 0.98 precision and 0.93 recall on malignant cases.

## What the notebook covers

1. **Understanding the data:** distributions, skewness and kurtosis of key features.
2. **Preprocessing:** dropping an empty column and the ID column, encoding the diagnosis (M = 1, B = 0), and standardising features.
3. **Exploratory analysis:** class balance and a correlation heatmap.
4. **Modelling:** a 70/30 train/test split, Logistic Regression, then a Random Forest for comparison.
5. **Feature selection experiment:** keeping only the most correlated features *hurt* performance. Correlation with the target alone was not a good basis for removing features.

In cancer screening a false negative (missing a malignant tumour) is the costly error, so models are compared on that as well as accuracy.

## Run it

```bash
pip install pandas numpy scipy scikit-learn matplotlib seaborn jupyter
jupyter notebook breast_cancer_classifier.ipynb
```

## Built with

Python · pandas · NumPy · SciPy · scikit-learn · Matplotlib · seaborn · Google Colab

## Dataset

`data.csv` is the [Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) by W.H. Wolberg, W.N. Street and O.L. Mangasarian, University of Wisconsin. It is redistributed unchanged under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
