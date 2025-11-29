📌 Project Highlights

Detects and classifies malicious URLs

Multi-class output: Benign, Phishing, Malware, Defacement

Final accuracy: 98.8%

Uses Stacking Ensemble approach

Real-time URL prediction with CLI

🧠 Models Used

Random Forest

Handles noisy data well

Good baseline accuracy

LightGBM

Fast and memory efficient

XGBoost

Handles complex patterns in features

CatBoost

Reduces overfitting on categorical features

Logistic Regression (Meta-Model)

Combines predictions from all 4 models

Chooses final label based on highest probability

🎯 Why Stacking?

Each model has unique strengths

Combines multiple predictions → better generalization

Reduces false positives vs single models

Final logistic regression ensures stable and accurate decision-making

📊 Accuracy Results

Random Forest → 98.5%

LightGBM → 96.6%

XGBoost → 96.9%

CatBoost → 97.2%

Stacking Model → 98.8% (Best)

⚙ How Prediction Works

Input URL given by user

Extracts lexical + structural features from URL

Base models generate class probability outputs

Logistic meta-model evaluates and decides final class

Returns predicted class + confidence score

📁 Dataset Details

Malicious URL dataset (~6.5 Lakh records)

4 label classes used

Extracted features include:

URL length

Presence of IP

Count of symbols (/, @, -, ?, %, =, .)

Suspicious keyword flags (e.g., login, secure, update)

🛠 Technologies Used

Language: Python

Libraries: pandas, scikit-learn, XGBoost, LightGBM, CatBoost, tqdm

Model Saved: .sav format

OS Support: Windows/Linux/Mac

▶ How to Use

Install dependencies:

pip install -r requirements.txt


Train the model:

python malicious_stack.py --train


Test a URL:

python malicious_stack.py --url "https://example.com"

💡 Features

High-speed prediction

Multi-class detection

Out-of-fold training reduces overfitting

CLI-based deployment ready

Can be extended into:

Web App

Chrome Extension

SOC Analyst Tool

🔮 Future Scope

Add DNS + WHOIS + HTML content-based detection

Deep Learning enhancements (LSTM/CNN)

Cloud deployment with REST API

Browser plugin for live URL monitoring

Explainability module (Why URL was blocked)
