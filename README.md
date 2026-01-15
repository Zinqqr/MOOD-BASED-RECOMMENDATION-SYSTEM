# 🎬 Mood-Based Movie Recommendation System (LLM-Inspired)

## 📌 Project Overview
This project implements a **mood-based movie recommendation system** that suggests movies based on a user’s emotional state expressed in natural language.  
Instead of relying on historical user data, the system infers mood from text input and recommends movies accordingly, effectively addressing the **cold-start problem**.

The project follows a **rule-based NLP approach inspired by Large Language Model (LLM) reasoning**, ensuring cost-effectiveness, reproducibility, and ethical deployment.

---

## 🎯 Problem Definition & Objective

### 🔹 Selected Track
**AI / NLP / Recommendation Systems**

### 🔹 Problem Statement
Users often struggle to select movies due to content overload on streaming platforms. Traditional recommender systems depend heavily on user history, making them ineffective for new users.

### 🔹 Objective
To design a **natural language mood-based recommendation system** that:
- Accepts free-text user input
- Infers emotional intent (mood)
- Recommends relevant movies without requiring prior user data

### 🔹 Real-World Relevance
- Solves the cold-start problem
- Enhances user experience through personalization
- Applicable to streaming platforms, chatbots, and AI assistants

---

## 📊 Data Understanding & Preparation

### 🔹 Dataset Source
- **TMDB 5000 Movies Dataset**
- Publicly available
- No personal or sensitive user data

### 🔹 Dataset Contents
- Movie title
- Genres (JSON format)
- Overview (description)
- Vote average (rating)
- Popularity score

### 🔹 Data Processing Steps
- Loaded dataset using `pandas`
- Parsed genre information using `ast.literal_eval`
- Converted genres into list format for filtering
- Created derived features such as `genre_list` and `genre_names`

### 🔹 Data Quality Handling
- Dataset contains minimal missing values
- No user-generated noise
- Suitable for content-based recommendation

---

## 🧠 Model / System Design

### 🔹 AI Technique Used
- **Natural Language Processing (rule-based)**
- **Content-based recommendation**
- **LLM-inspired reasoning (simulation)**

### 🔹 Design Justification
> Due to API access constraints, the system implements a **rule-based natural language understanding module** to simulate LLM-style reasoning for mood extraction.  
> This approach ensures reproducibility, cost-effectiveness, and ethical deployment while preserving the core recommendation logic.

### 🔹 System Pipeline
1. User inputs mood as text
2. Mood is extracted using keyword-based NLP
3. Mood is mapped to relevant genres
4. Movies are filtered by genres
5. Results are ranked by rating and popularity

---

## ⚙️ Core Implementation

### 🔹 Mood Extraction
- Rule-based keyword matching
- Supports moods such as:
  - Happy
  - Sad
  - Angry
  - Relaxed
  - Excited
  - Scared
  - Neutral (fallback)

### 🔹 Recommendation Engine
- Filters movies using mood-to-genre mapping
- Ranks results using:
  - Vote average
  - Popularity score

### 🔹 Conversational Extension
- Asks follow-up preference (light / intense)
- Dynamically adjusts recommendations

### 🔹 UI Implementation
- Built using **Streamlit**
- Interactive web interface
- Real-time recommendations

### 🔹 Code Reliability
✅ Runs top-to-bottom without errors  
✅ Modularized (`recomender.py`, `app.py`)  
✅ Dataset loaded dynamically using relative paths  

---

## 📈 Evaluation & Analysis

### 🔹 Evaluation Approach
- **Qualitative evaluation**
- Manual inspection of recommendations
- Mood-to-genre alignment analysis

### 🔹 Sample Output
Input:"I feel stressed and want something calm"
Detected Mood:Relaxed
Recommended Genres:Drama, Fantasy


### 🔹 Observations
- Recommendations align well with emotional context
- Handles new users effectively
- Rule-based approach limits nuanced emotion detection

### 🔹 Limitations
- Mood detection depends on predefined keywords
- Cannot detect complex emotional expressions
- No learning from user feedback

---

## ⚖️ Ethical Considerations & Responsible AI

### 🔹 Bias & Fairness
- No user profiling
- No demographic or behavioral bias
- Content-based filtering only

### 🔹 Dataset Limitations
- Popularity bias toward well-known movies
- Limited representation of niche cinema

### 🔹 Responsible AI Practices
- No personal data usage
- Transparent logic
- Fully explainable recommendations

---

## ✅ Conclusion & Future Scope

### 🔹 Conclusion
The project successfully demonstrates a **mood-based recommendation system** that:
- Works without historical data
- Uses explainable NLP logic
- Provides meaningful personalization

### 🔹 Future Enhancements
- Replace rule-based mood extraction with real LLM APIs
- Use sentiment analysis models (BERT / GPT)
- Add user feedback learning
- Deploy with cloud storage and caching

---

## 🚀 How to Run the Project

### Run Streamlit App

Follow the steps below to run the application locally:
- cd "mood based recommendation system"
- python recomender.py
- python -m streamlit run app.py

## 📂 Project Structure
mood-based-recommendation-system/
│
├── app.py  
├── recomender.py  
├── data/  
│   └── tmdb_5000_movies.csv  
├── README.md  


---

✨ This project emphasizes clarity, ethical AI use, and real-world applicability over black-box automation.
