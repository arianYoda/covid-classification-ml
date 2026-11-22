# COVID-19 Classification — Machine Learning

## Overview

This project explores binary classification using machine learning to predict whether a person has COVID-19 based on four features: Age, Gender, Fever, and Cough.

Six classification approaches were evaluated and compared using multiple performance metrics.



## Dataset

The dataset contains 986 records and five columns: four input features and one target variable.

### Features

* **Age:** Age of the person.
* **Gender:** Gender encoded as a binary value.
* **Fever:** Body temperature.
* **Cough:** Cough status encoded as a binary value.

### Target

* **Has_Covid:** Indicates whether the person has COVID-19 (`1`) or does not have COVID-19 (`0`).

The dataset contains 510 records labeled `0` and 476 records labeled `1`.



## Models

The following six classification approaches were trained and evaluated:

1. **K-Nearest Neighbors (KNN)**
2. **Logistic Regression**
3. **Decision Tree**
4. **Scaled KNN** — KNN trained using standardized features.
5. **Random Forest**
6. **Support Vector Machine (SVM)**

`StandardScaler` was used to standardize features for the scaled KNN and SVM models. The models were evaluated on a held-out test set.



-- Evaluation Metrics

The models were evaluated using the following metrics:

* **Accuracy:** The proportion of correct predictions.
* **Precision:** How many predicted positive cases were actually positive.
* **Recall:** How many actual positive cases the model correctly identified.
* **F1-score:** The harmonic mean of precision and recall.
* **ROC-AUC:** Measures how well a model distinguishes between the two classes across different classification thresholds.

--- Results

The models showed relatively weak classification performance on the test set. SVM achieved the highest AUC (0.4936), while Logistic Regression achieved the highest accuracy (0.5000).

The AUC scores were close to 0.5, suggesting that the models struggled to distinguish COVID-19 and non-COVID-19 cases using the available features.



## Installation and Usage

### 1. Clone the repository

```bash
git https://github.com/arianYoda
```



### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

Open `covid_classification.ipynb` in Jupyter Notebook or VS Code.

### 4. Run the project

Run the notebook cells from top to bottom. Make sure `covid_dataset_simple.csv` is in the same directory as the notebook.



## Project Files

* `covid_classification.ipynb` — Notebook containing data exploration, model training, evaluation, and visualizations.
* `covid_dataset_simple.csv` — Dataset used for the classification experiments.
* `requirements.txt` — Python dependencies required to run the project.
* `README.md` — Project description, methodology, results, and usage instructions.

## Limitations

The models achieved weak classification performance on the test set. The available features may not contain enough information to reliably distinguish between the two classes.

This project is an educational machine learning exercise and is **not intended for medical diagnosis or real-world COVID-19 screening**.
