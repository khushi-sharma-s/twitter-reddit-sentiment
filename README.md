# Sentiment Analysis of Reddit and Twitter 📊🤖

A Machine Learning and Natural Language Processing (NLP) project that collects, cleans, and analyzes user reviews and sentiments from both Twitter and Reddit. The model classifies the data to understand the overall public opinion and feedback across different social media platforms.

---

## 🚀 Project Overview
Social media platforms like Twitter and Reddit are rich sources of consumer opinions. This project combines datasets from both platforms to train a sentiment classification model. It handles challenges like platform-specific slangs, hashtags, URLs, and emojis to deliver clean, actionable sentiment insights.

## 🛠️ Tech Stack & Libraries
- **Language:** Python 🐍
- **Environment:** Jupyter Notebook 📓
- **NLP Libraries:** NLTK, Regular Expressions (Re)
- **Machine Learning:** Scikit-Learn (Logistic Regression, TF-IDF Vectorizer)
- **Data Manipulation:** Pandas, NumPy

---

## 📂 Project Structure
```text
├── Data/
│   ├── twitter_reviews.csv       # Raw Twitter dataset
│   └── reddit_reviews.csv        # Raw Reddit dataset
├── Twitter_Reddit_Sentiment_Analysis.ipynb  # Main Jupyter Notebook
├── README.md                     # Project documentation
└── requirements.txt              # Required Python packages
```

---

## ⚙️ Key Features & Workflow

1. **Data Preprocessing & Cleaning:**
   - Converts text to lowercase.
   - Removes URLs, HTML tags, punctuation, and numbers.
   - Strips out Twitter handles (`@username`) and Reddit community tags (`r/` or `u/`).
   - Filters out English stopwords using NLTK.

2. **Feature Extraction:**
   - Converts cleaned text into numerical vectors using **TF-IDF Vectorization** (Term Frequency-Inverse Document Frequency) with up to 5,000 top features.

3. **Model Training:**
   - Splits the integrated dataset into an 80:20 Train-Test ratio.
   - Trains a high-performance **Logistic Regression** classifier suited for text heavy-lifting.

4. **Inference pipeline:**
   - Includes a custom prediction function to test live tweets or Reddit comments on the fly.

---

## 💻 How to Run Locally

### 1. Clone the Repository
```bash
git clone https://github.com
cd social-media-review-analyzer
```

### 2. Install Dependencies
```bash
pip install pandas numpy scikit-learn nltk
```

### 3. Run the Jupyter Notebook
```bash
jupyter notebook
```
Open `Twitter_Reddit_Sentiment_Analysis.ipynb` and execute the cells sequentially.

---

## 📈 Sample Inference Output
```python
>>> predict_new_review("I absolutely love how this new update works on the platform!")
👉 Prediction: Positive Sentiment 😊

>>> predict_new_review("The lag in this application makes it completely unusable.")
👉 Prediction: Negative Sentiment 😡
```

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to improve the text cleaning process or test advanced models like BERT/LSTM.
