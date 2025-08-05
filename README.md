# 🧠 Personality Prediction from Text using NLP & Machine Learning

This project uses Natural Language Processing (NLP) and Machine Learning to predict personality types based on written text. The classification is based on the MBTI (Myers–Briggs Type Indicator) model, trained on real MBTI posts.

## 📌 Features

- ✅ MBTI personality type prediction (e.g., INTJ, ENFP, ISTP)
- ✅ Preprocessing using SpaCy (lemmatization, stopword removal)
- ✅ Feature extraction with TF-IDF vectorizer
- ✅ Model training using Logistic Regression
- ✅ Dataset balancing with SMOTE
- ✅ Streamlit UI + Ngrok tunnel integration for online access

## 🛠️ Tech Stack

- Python
- SpaCy (`en_core_web_sm`)
- scikit-learn
- imbalanced-learn (SMOTE)
- Streamlit
- Pyngrok (for public URL)

## 🗃️ Dataset

- **File:** `mbti_1.csv`
- **Source:** MBTI type labeled text data (user posts)
- **Format:**
  - `type` → MBTI label (e.g., INFJ)
  - `posts` → Text samples for each user

## 🧪 Model Pipeline

1. **Text Cleaning:** Lowercasing, URL and punctuation removal
2. **Lemmatization:** Using SpaCy
3. **Vectorization:** TF-IDF with max 5000 features
4. **Balancing:** SMOTE to address class imbalance
5. **Training:** Logistic Regression
6. **Prediction:** Custom `predict_personality(text)` function

## 💻 How to Run the Project

## Upload Dataset to Colab:

/content/drive/MyDrive/mbti_1.csv

## Run Streamlit App:

streamlit run app.py

## Expose Public URL (Ngrok):

from pyngrok import ngrok
ngrok.set_auth_token("your_token_here")

1. **Install Requirements:**

pip install spacy scikit-learn imbalanced-learn streamlit pyngrok
python -m spacy download en_core_web_sm

## 🖼 Sample Input

I love deep intellectual conversations and enjoy thinking about abstract concepts.

## ✅ Predicted Output:

INTP (Introverted, Intuitive, Thinking, Perceiving)
