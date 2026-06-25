# Multimodal-Comment-Classification-using-TF-IDF-and-LightGBM

## Overview

This project was developed for the Kaggle **Comment Category Prediction Challenge**.

The objective is to predict the final category assigned to user-generated comments using a combination of:

* Natural language content
* User engagement signals
* Emoticon indicators
* Platform-generated metadata

Unlike traditional text classification problems, this task combines textual and structured information, making it a multimodal machine learning problem.

---

## Dataset Features

### Text Features

* Comment text

### User Interaction Features

* Upvotes
* Downvotes

### Symbolic Features

* Emoticon indicators

### Platform Signals

* Internal system features
* Topic indicators

---

## Feature Engineering

### Text Processing

* Lowercasing
* URL removal
* Text normalization

### TF-IDF Features

#### Word-Level TF-IDF

* 30,000 features
* Unigrams and Bigrams

#### Character-Level TF-IDF

* 20,000 features
* Character n-grams (2–4)

### Numerical Features

* Comment length
* Upvotes
* Downvotes
* Emoticon indicators
* Platform-generated signals

Final feature space:

* 50,008 engineered features

---

## Models Evaluated

| Model          | Macro F1 Score |
| -------------- | -------------- |
| Dummy Baseline | 0.57           |
| Linear SVM     | 0.68           |
| SGD Classifier | 0.71           |
| LightGBM       | 0.83           |

---

## Best Model

### LightGBM

Configuration:

* Multiclass objective
* 500 estimators
* Early stopping
* Balanced sample weights
* Feature subsampling
* Row subsampling

### Performance

* Validation Accuracy: 92%
* Macro F1 Score: 0.831

---

## Key Findings

The results indicate that:

* Text features alone are insufficient
* Metadata contributes significantly to prediction performance
* Character-level TF-IDF improves robustness
* LightGBM effectively captures non-linear interactions between textual and structured features

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* LightGBM
* SciPy
* Matplotlib
* Seaborn

---

## Project Structure

```text
project/
│
├── notebooks/
│   └── Comment_Classification.ipynb
│
├── images/
│   └── eda_charts.png
│
├── requirements.txt
├── README.md
└── submission.csv
```

## Future Improvements

* Transformer-based models (BERT, RoBERTa)
* Ensemble learning
* Advanced text embeddings
* Hyperparameter optimization
* Stacking multiple classifiers

## Author

Nandu

IIT Madras Online Degree Program – Data Science
Machine Learning | NLP | Applied AI
