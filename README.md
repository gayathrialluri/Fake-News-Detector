**FAKE NEWS DETECTION USING MACHINE LEARNING**

This project classifies news articles as Fake or Real using TF-IDF text features and two machine-learning models — Naive Bayes and Random Forest.
It includes full preprocessing, training, evaluation, cross-validation, and feature-importance visualization.

📂 **Project Structure**

├─ FakeNewsDetection.ipynb
├─ True.csv
├─ Fake.csv
├─ requirements.txt
└─ README.md

🧠 **Workflow Overview**
1.Data Preparation

• Load True.csv and Fake.csv  

• Assign labels: 1 = Real, 0 = Fake  

• Shuffle and combine the datasets  

• Merge title + text into a single input field (content)  


2.Text Processing with TF-IDF

• Convert text into numerical vectors
• Remove English stopwords
• Use max_df = 0.7 to reduce noise
• Split into train/test sets (80/20)

3.Machine Learning Models

Trained two ML models:

• Multinomial Naive Bayes
• Random Forest Classifier (100 trees)

📊 **Model Evaluation Metrics**

1. Accuracy

Computed for both models using:
accuracy_score(y_test, predictions)

2. Confusion Matrix
confusion_matrix(y_test, predictions)

3. Precision, Recall & F1-Score

Generated through:
classification_report(y_test, predictions)

4. 5-Fold Cross Validation (Accuracy)

Applied to both Naive Bayes and Random Forest:

cross_val_score(model, X_train_vec, y_train, cv=5)

5. Feature Importance (Random Forest)

• Extract top 20 TF-IDF features
• Visualize as a horizontal bar plot

🧪**Results Summary**

• Naive Bayes Results
• Random Forest Results
• Accuracy for both models
• Confusion Matrix
• Precision / Recall / F1-Score
• 5-fold CV mean accuracy
• Top 20 most important TF-IDF features (Random Forest)



▶️**How to Run the Project**
Install dependencies
pip install -r requirements.txt

Run the notebook
jupyter notebook FakeNewsDetection.ipynb

Make sure True.csv and Fake.csv are in the same directory.

🗂️ **Dataset**

The project uses two labeled datasets:

• True.csv → Real news
• Fake.csv → Fake news

These datasets contain title, text, subject, and date fields.

