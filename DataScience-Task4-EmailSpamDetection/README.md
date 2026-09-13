# Task 4 — Email Spam Detection with Machine Learning

## Project Overview

This project develops an NLP-based binary classification system to distinguish **spam** messages from legitimate **ham** messages using the SMS Spam Collection Dataset.

The project follows a complete machine learning workflow including data cleaning, text preprocessing, TF-IDF feature extraction, model training, evaluation, and model comparison.

## Objective

Build a Natural Language Processing (NLP) classifier that distinguishes spam messages from legitimate (ham) messages.

## Tech Stack

- Python
- pandas
- scikit-learn
- NLTK
- re
- matplotlib
- seaborn
- Jupyter Notebook

## Dataset

**SMS Spam Collection Dataset**

The dataset contains labeled SMS messages with two classes:

- `ham` — legitimate messages
- `spam` — unwanted messages

After duplicate and empty-message removal, the final dataset contained **5,164 messages**:

| Class | Count | Percentage |
|---|---:|---:|
| Ham | 4,511 | 87.35% |
| Spam | 653 | 12.65% |

## Workflow

Dataset → Cleaning → Text Preprocessing → Train/Test Split → TF-IDF → 3 Models → Evaluation → Best Model → Confusion Matrix → WordCloud

## Data Preprocessing

The text preprocessing pipeline includes:

- Lowercase conversion
- Punctuation removal
- Whitespace cleanup
- Stopword removal
- Duplicate removal
- Removal of messages that became empty after preprocessing

## Feature Extraction

**TF-IDF (Term Frequency-Inverse Document Frequency)** was used to convert text into numerical features.

The vectorizer was fitted only on the training data and then used to transform the test data to avoid data leakage.

Final TF-IDF representation:

- Training samples: 4,131
- Testing samples: 1,033
- TF-IDF features: 8,229

## Machine Learning Models

Three classifiers were trained and compared:

1. **Multinomial Naive Bayes**
2. **Logistic Regression**
3. **Linear SVM**

## Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Multinomial Naive Bayes | 96.71% | 100.00% | 74.05% | 85.09% |
| Logistic Regression | 95.16% | 94.51% | 65.65% | 77.48% |
| **Linear SVM** | **98.45%** | **97.52%** | **90.08%** | **93.65%** |

### Best Model

**Linear SVM** achieved the highest F1-score and was selected as the best-performing classifier.

Its performance:

- Accuracy: **98.45%**
- Precision: **97.52%**
- Recall: **90.08%**
- F1 Score: **93.65%**

## Why Recall Matters

Recall is particularly important in spam detection because a false negative means an actual spam message is classified as legitimate.

A higher recall means the classifier can identify a larger proportion of actual spam messages, reducing the number of spam messages that pass through as legitimate messages.

## Visualizations

The project includes:

- Spam vs. ham class distribution
- Confusion matrix for the best-performing model
- Spam WordCloud
- Ham WordCloud

## Repository Structure

```text
OIBSIP/
└── DataScience-Task4-EmailSpamDetection/
    ├── Task4_Email_Spam_Detection.ipynb
    ├── README.md
    └── outputs/
        ├── model_comparison.csv
        └── figures/
            ├── confusion_matrix_linear_svm.png
            ├── spam_wordcloud.png
            └── ham_wordcloud.png
