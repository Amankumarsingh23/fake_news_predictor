# 📰 Fake News Prediction using Machine Learning

This project is a **Fake News Detection System** built using **Python**, **Logistic Regression**, and **Natural Language Processing (NLP)** techniques.  
It classifies news articles as **Real** or **Fake** based on their content.

---

## 📌 Problem Statement

In today’s digital world, misinformation spreads faster than ever.  
The goal of this project is to build a machine learning model that can classify news articles as **real** or **fake**, helping to combat the spread of false information.

---

## 📂 Dataset Overview

- **Source**: [Kaggle - Fake News Dataset](https://www.kaggle.com/c/fake-news)
- **Instances**: ~20,000+
- **Features**: Author, Title, Text, Label
- **Labels**: 
  - `0` → Real News  
  - `1` → Fake News

---

## ⚙️ Tech Stack & Libraries

- **Python**
- **NumPy**
- **Pandas**
- **NLTK** (Stopwords, Stemming)
- **Scikit-learn**
  - LogisticRegression
  - TfidfVectorizer

---

## 🚀 Workflow

1. **Data Collection**
   - Load dataset into a Pandas DataFrame

2. **Data Preprocessing**
   - Handle missing values
   - Merge `author` and `title` columns into `content`
   - Apply **stemming** & **stopword removal**
   - Convert text to lowercase & remove special characters

3. **Feature Extraction**
   - Use **TF-IDF Vectorization** to transform text into numerical features

4. **Model Training**
   - Logistic Regression Classifier

5. **Model Evaluation**
   - Accuracy Score on Training and Test Data

6. **Prediction System**
   - Input: A news article  
   - Output: Real or Fake

---

## 📊 Model Performance

| Metric              | Score      |
|---------------------|------------|
| Training Accuracy   | ~98%       |
| Test Accuracy       | ~96%       |

---

## 💡 Sample Prediction

```python
x_news = X_test[186]
prediction = model.predict(x_news)

if prediction[0] == '0':
    print("The news is Real")
else:
    print("The news is Fake")
