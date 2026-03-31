# Cyber-Bullying Prediction

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![NLTK](https://img.shields.io/badge/NLTK-3.6+-green.svg)](https://www.nltk.org/)

## 📌 Overview

This project detects cyberbullying in Formspring Q&A posts using **Natural Language Processing (NLP)** and **Machine Learning**. The system preprocesses text data, extracts features using TF-IDF vectorization, and classifies posts using multiple algorithms with hyperparameter tuning via GridSearchCV.

## 🎯 Problem Statement

Cyberbullying has become a critical issue on social media platforms. This project aims to automatically identify bullying content in Formspring posts to help platforms moderate harmful content and protect users.

## 📊 Dataset

- **Source**: Formspring social platform Q&A entries
- **Size**: 13,147 text entries
- **Format**: CSV file with labeled posts (bullying vs. non-bullying)
- **Challenge**: Highly imbalanced dataset with majority non-bullying samples

## 🛠️ Tech Stack

| Category | Libraries/Tools |
|----------|----------------|
| **Data Processing** | pandas, numpy |
| **NLP** | NLTK (stopwords, SnowballStemmer) |
| **Machine Learning** | scikit-learn (TfidfVectorizer, GridSearchCV, SVC, MultinomialNB, DecisionTreeClassifier, LogisticRegression, RidgeClassifier, SGDClassifier, LabelEncoder) |
| **Visualization** | matplotlib |

## 🔧 Methodology

### 1. Text Preprocessing
- Stopword removal
- Stemming using SnowballStemmer
- Text cleaning and normalization

### 2. Feature Extraction
- TF-IDF (Term Frequency-Inverse Document Frequency) vectorization
- Converting text data into numerical features

### 3. Model Training & Optimization
- Multiple classifiers evaluated:
  - Support Vector Classifier (SVC)
  - Multinomial Naive Bayes
  - Decision Tree
  - Logistic Regression
  - Ridge Classifier
  - SGD Classifier
- Hyperparameter tuning using **GridSearchCV** with cross-validation

## 📈 Results

| Model | Accuracy | Precision | Recall |
|-------|----------|-----------|--------|
| **SVC (sigmoid kernel)** | 95.08% | 80.52% | 25.73% |
| **Multinomial Naive Bayes** | 94.02% | 53.62% | 15.35% |
| **Decision Tree** | 93.11% | 41.88% | 33.20% |

> **Note**: The dataset is significantly imbalanced (majority non-bullying samples). While accuracy appears high, the **low recall scores** indicate the models struggle to identify bullying content. This highlights the need for techniques like SMOTE, class weighting, or more sophisticated NLP approaches.

## 🚀 How to Run

### Prerequisites
```bash
Python 3.7 or higher
```
Clone the repository
```
git clone https://github.com/yourusername/cyber-bullying-prediction.git
cd cyber-bullying-prediction
```
Install dependencies
```
pip install pandas numpy nltk scikit-learn matplotlib
```
Download NLTK data
```
python -c "import nltk; nltk.download('stopwords')"
```
## 📁 Project Structure
```
cyber-bullying-prediction/
├── cyber_bullying.ipynb   # Main Jupyter notebook
├── Formspring.csv          # Dataset file
├── README.md              # Project documentation
└── requirements.txt       # Dependencies list
```
⭐ Star this repository if you found it useful!

This markdown provides a professional, well-structured README for your GitHub project with:
- Clear sections and formatting
- Visual badges for technology stack
- Tables for results and tech stack
- Code blocks for installation commands
- Future improvement suggestions
- Professional presentation suitable for a portfolio project

