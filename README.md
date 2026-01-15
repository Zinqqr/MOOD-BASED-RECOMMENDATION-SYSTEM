# 🎬 Mood-Based Movie Recommendation System

This project is a **Natural Language–driven movie recommendation system** that suggests movies based on a user's emotional state expressed in text.

---

## 🚀 Features
- Mood detection from natural language
- Content-based movie recommendations
- Cold-start problem handling
- Interactive Streamlit UI

---

## 🧠 System Design
- **NLP (Rule-based mood extraction)**
- **Content-based recommendation**
- **Streamlit frontend**

> Due to API access constraints, a rule-based natural language understanding module is used to simulate LLM-style reasoning. This ensures reproducibility and cost-effectiveness.

---

## 📂 Dataset
- TMDB 5000 Movies Dataset
- Source: Kaggle
- Contains movie metadata (genres, ratings, popularity)

---

## ▶️ How to Run Locally

```bash
pip install -r requirements.txt
streamlit run app.py
