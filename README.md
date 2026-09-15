# Titanic Survival Prediction

A binary classification project that predicts whether a Titanic passenger survived using **Python, Pandas, and Scikit-learn**.

## Results

| Metric | Score |
|---|---:|
| **Test Accuracy** | **80.45%** |
| **F1 Score** | **72.44%** |

## Project Overview

The objective is to build and evaluate a machine learning model that predicts passenger survival from demographic and ticket-related features.

The project follows an end-to-end machine learning workflow: data exploration, preprocessing, train/test splitting, model training, and evaluation.

## Tech Stack

- Python
- Pandas
- Scikit-learn
- Seaborn
- Matplotlib
- Google Colab

## Dataset

The Titanic dataset was loaded using Seaborn's built-in dataset collection. It contains passenger information and a binary `survived` target.

### Target Variable

- `0` — Did not survive
- `1` — Survived

## Features Used

- `pclass` — Passenger class
- `sex` — Passenger sex
- `age` — Passenger age
- `sibsp` — Number of siblings/spouses aboard
- `parch` — Number of parents/children aboard
- `fare` — Passenger fare
- `embarked` — Port of embarkation

## Machine Learning Workflow

1. Loaded and inspected the Titanic dataset
2. Identified missing values and data types
3. Selected relevant features
4. Split the dataset into 80% training and 20% testing data
5. Used median imputation for numerical missing values
6. Used most-frequent imputation for categorical missing values
7. Applied one-hot encoding to categorical features
8. Combined preprocessing and model training using `Pipeline` and `ColumnTransformer`
9. Trained a Logistic Regression classifier
10. Evaluated predictions using accuracy, F1 score, and a confusion matrix

## Model

**Logistic Regression** was selected as the baseline classifier because the target is binary.

The final implementation uses a Scikit-learn `Pipeline` and `ColumnTransformer`. Preprocessing is fitted on the training data and then applied to the test data, helping prevent data leakage.

## Evaluation

### Test Performance

- **Accuracy:** 80.45%
- **F1 Score:** 72.44%

### Confusion Matrix

```text
                    Predicted
                  Did Not   Survived
                  Survive

Actual Did Not      98        12
       Survive

       Survived     23        46
```

The confusion matrix shows the model's true positives, true negatives, false positives, and false negatives on the unseen test set.

## Project Structure

```text
titanic-survival-ml/
├── Titanic_Survival_ML.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Ani2828/titanic-survival-ml.git
cd titanic-survival-ml
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

Open `Titanic_Survival_ML.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab and run the cells.

## Key Learning Outcomes

- Data cleaning and missing-value handling
- Categorical feature encoding
- Train/test splitting
- Preventing preprocessing leakage
- Building Scikit-learn pipelines
- Classification model evaluation
- Interpreting accuracy, F1 score, and confusion matrices

## Conclusion

The Logistic Regression model achieved **80.45% test accuracy** and a **72.44% F1 score** on the Titanic dataset. The project demonstrates a complete and reproducible machine learning classification workflow from raw data to model evaluation.
