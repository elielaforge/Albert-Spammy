# 🛡️ YouTube Spam Detector: Business-Ready ML for Content Moderation
<p align="center">
  <strong>Elie LAFORGE, Yunan WANG</strong><br>
  Albert School – 2024
</p>



This repository presents a complete end-to-end machine learning solution to detect **spam comments on YouTube**, using supervised learning techniques and NLP. The goal is to **protect digital spaces**, **reduce moderation burden**, and **enhance user trust** through automated, scalable solutions.

---

## 📌 Business Context

As video platforms like YouTube grow, **spam comments have become a real threat** to content quality and user engagement. Brands, creators, and platform moderators often lack the time or tools to filter through thousands of irrelevant or malicious messages. The cost of inaction? ⛔ Decreased user trust, lost engagement, and reputational damage.

**This project delivers a scalable solution** using Natural Language Processing and Machine Learning to automatically classify spam vs. legitimate comments — helping businesses and platforms:

- Reduce human moderation costs
- Prevent scams and phishing content
- Improve community safety and experience

---

## 🎯 Objective

> Automatically detect spam in YouTube comments using machine learning on a labeled dataset.

---

## 📦 Dataset

- Source: Kaggle – “YouTube Spam Collection” dataset & 5000 YT comments
- Structure: 7,000+ labeled comments  
- Target variable: `CLASS` (1 = Spam, 0 = Not Spam)  
- Columns: `comment_id`, `author`, `date`, `content`, `video_id`, `CLASS`

The dataset was relatively balanced:  
- **Spam**: 48.6%  
- **Not Spam**: 51.4%

---

## 🧪 Exploratory Analysis

Key patterns found in spam comments:

- Frequent use of words like “check”, “subscribe”, “video”, “channel”, “new mixtape”  
- High presence of promotional or deceptive keywords

Word cloud analysis revealed repetitive promotional language, ideal for machine learning classification.

---

## 🧼 Preprocessing

Steps included:

- Removing duplicates and nulls
- Text normalization and tokenization
- TF-IDF vectorization (with tuned parameters)

---

## 🤖 Models Compared

| Metric      | Logistic Regression | Naive Bayes | XGBoost |
|-------------|---------------------|-------------|---------|
| Accuracy    | 0.90                | 0.78        | 0.90    |
| F1-Score    | 0.89                | 0.73        | 0.89    |
| ROC-AUC     | 0.95                | 0.90        | 0.96    |

---

## ✅ Best Performing Model: XGBoost

After hyperparameter tuning, **XGBoost** delivered the highest performance:

- **Accuracy**: 95%
- **F1-Score**: 95%
- **ROC-AUC**: 0.98  
- **Confusion Matrix**: True positive detection was very strong (500 spam comments correctly identified)

---

## 🧠 Business Takeaways

- ⚙️ **Efficient automation**: ML cuts down the need for manual spam moderation
- 🔒 **Protects brand & users**: Automatically filters misleading or harmful links
- 💰 **Scalability**: Solution works on any large volume of user-generated content
- 📈 **Immediate deployment potential**: Results are production-grade with minimal latency

> A solution like this could be embedded into YouTube’s backend or offered as a third-party moderation API.

---

## 📁 Repository Structure

