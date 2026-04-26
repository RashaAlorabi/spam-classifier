# 📧 SMS Spam Classifier

A Machine Learning model that classifies SMS messages as **spam** or **ham** using Logistic Regression and NLP techniques. Achieves **98.7% accuracy** on real-world data.

---

## 🎯 What It Does

```
Input:  "Congratulations! You won a FREE iPhone. Click now!"
Output: 🚨 SPAM (confidence: 97.3%)

Input:  "Hey, are we still meeting tomorrow for lunch?"
Output: ✅ HAM (confidence: 99.1%)
```

---

## 📊 Results

| Metric | Ham | Spam |
|--------|-----|------|
| Precision | 0.99 | 0.98 |
| Recall | 0.99 | 0.97 |
| F1-Score | 0.99 | 0.97 |
| **Accuracy** | **0.987** | |

---

## 🏗️ Pipeline

```
5,572 Real SMS Messages
      ↓
Text Preprocessing
      ↓
CountVectorizer (500 features)
      ↓
Train/Test Split (80/20)
      ↓
Logistic Regression Training
      ↓
Evaluation (Precision, Recall, F1, Confusion Matrix)
      ↓
Interactive Spam Detector
```

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| ML Model | scikit-learn LogisticRegression |
| NLP | CountVectorizer |
| Data | UCI SMS Spam Collection (5,572 messages) |
| Visualization | Matplotlib, Seaborn |
| Language | Python 3.11 |

---

## 📦 Installation

```bash
git clone https://github.com/RashaAlorabi/spam-classifier.git
cd spam-classifier

python3 -m venv ai-env
source ai-env/bin/activate

pip install -r requirements.txt
```

---

## 🚀 Usage

```bash
jupyter notebook spam_classifier.ipynb
```

Test your own messages:

```python
predict_spam("Free money click here!")
# Output: SPAM (confidence: 98.2%)

predict_spam("Meeting at 3pm today")
# Output: HAM (confidence: 99.7%)
```

---

## 🔑 Key Learnings

- **CountVectorizer** — Converts text to numerical features (word counts)
- **Precision vs Recall** — False Negatives (missed spam) vs False Positives (blocked ham)
- **Class Imbalance** — Dataset had 87% ham vs 13% spam
- **Distribution Shift** — Model struggled with Arabic text (trained on English only)

---

## 🧠 Concepts Demonstrated

```
Text → Numbers:    CountVectorizer
Binary Output:     Logistic Regression + Sigmoid Function
Model Evaluation:  Confusion Matrix, Classification Report
Key Tradeoff:      Precision (don't block important emails)
                   vs Recall (don't miss spam)
```

---

## 📁 Project Structure

```
spam-classifier/
├── spam_classifier.ipynb   # Main notebook
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 📋 Requirements

```txt
scikit-learn
numpy
pandas
matplotlib
seaborn
jupyter
```

---

## 🚧 Future Improvements

- [ ] Add Arabic language support
- [ ] Try TF-IDF instead of CountVectorizer
- [ ] Build Telegram bot for real-time spam detection
- [ ] Deploy as API

---

## 👤 Author

**Rasha** — Senior Software Engineer → AI Solutions Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/YOUR_USERNAME)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/YOUR_USERNAME)