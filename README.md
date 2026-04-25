# 📧 SMS Spam Classifier
A Machine Learning model that classifies SMS messages as spam or ham using Logistic Regression and NLP techniques. Achieves 98.7% accuracy on real-world data.

🎯 What It Does
Input:  "Congratulations! You won a FREE iPhone. Click now!"
Output: 🚨 SPAM (confidence: 97.3%)

Input:  "Hey, are we still meeting tomorrow for lunch?"
Output: ✅ HAM (confidence: 99.1%)

📊 Results
MetricHamSpamPrecision0.990.98Recall0.990.97F1-Score0.990.97Accuracy0.987

🏗️ Pipeline
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

🛠️ Tech Stack
ComponentTechnologyML Modelscikit-learn LogisticRegressionNLPCountVectorizerDataUCI SMS Spam Collection (5,572 messages)VisualizationMatplotlib, SeabornLanguagePython 3.11

📦 Installation
bashgit clone https://github.com/RashaAlorabi/spam-classifier.git
cd spam-classifier

python3 -m venv ai-env
source ai-env/bin/activate

pip install -r requirements.txt

🚀 Usage
bashjupyter notebook spam_classifier.ipynb
Test your own messages:
pythonpredict_spam("Free money click here!")
# Output: SPAM (confidence: 98.2%)

predict_spam("Meeting at 3pm today")
# Output: HAM (confidence: 99.7%)

🔑 Key Learnings

CountVectorizer — Converts text to numerical features (word counts)
Precision vs Recall — False Negatives (missed spam) vs False Positives (blocked ham)
Class Imbalance — Dataset had 87% ham vs 13% spam
Distribution Shift — Model struggled with Arabic text (trained on English only)


🧠 Concepts Demonstrated
Text → Numbers:    CountVectorizer
Binary Output:     Logistic Regression + Sigmoid Function
Model Evaluation:  Confusion Matrix, Classification Report
Key Tradeoff:      Precision (don't block important emails)
                   vs Recall (don't miss spam)

📁 Project Structure
spam-classifier/
├── spam_classifier.ipynb   # Main notebook
├── requirements.txt
├── .gitignore
└── README.md

📋 Requirements
txtscikit-learn
numpy
pandas
matplotlib
seaborn
jupyter

🚧 Future Improvements

 Add Arabic language support
 Try TF-IDF instead of CountVectorizer
 Build Telegram bot for real-time spam detection
 Deploy as API


👤 Author
Rasha — Senior Software Engineer → AI Solutions Engineer