# 🩺 Diabetes Detection System

A machine learning-based classification system that predicts whether a person has diabetes using diagnostic data. This project explores multiple ML algorithms and evaluates their performance using key classification metrics and ROC curves.

---

## 📊 Features in the Dataset

- Pregnancies  
- Glucose  
- BloodPressure  
- SkinThickness  
- Insulin  
- BMI (Body Mass Index)  
- DiabetesPedigreeFunction  
- Age  
- Outcome – Target variable (0 = No Diabetes, 1 = Has Diabetes)

---

## 🧠 Models Used

- Logistic Regression  
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Random Forest  

---

## ⚙️ Project Workflow
1. Load the Dataset   
Data is loaded using pandas from a CSV file (diabetes.csv) containing 768 records with 8 features and 1 target.

3. Data Preprocessing  
Checked for null values.  
Standardized features using StandardScaler.  

3. Train-Test Split  
Dataset is split into 80% training and 20% testing using train_test_split.  

4. Model Training & Evaluation  

  Each model is trained and evaluated using:  
- Confusion Matrix  
- Classification Report  
- ROC-AUC Score  

5. ROC Curve Plotting  

All models' ROC curves are plotted on a single graph for comparison.

6. Model Performance Summary  

![Result](./Result.png)

---

## 📈 Visualizations

ROC curves comparing classifier performance  

![Output](./Output.png)  

Different problems require different evaluation strategies. Here's **why each metric fits best** in different scenarios:

| Scenario | Important Metric | Why? |
|----------|------------------|------|
| **Medical Diagnosis** | **Recall (avoid FN)** | Missing a disease (False Negative) is dangerous. Better to raise more false alarms (FP) than miss a real case. |
| **Spam Detection** | **Precision (avoid FP)** | Marking real emails as spam (False Positives) frustrates users. We want to be very sure before flagging something as spam. |
| **Balanced Task** | **F1 Score** | When both FP and FN are equally costly (e.g. Titanic survival), we need a balance between precision and recall. |
| **Marketing Campaign** | **Precision** | We'd rather send offers only to likely buyers. Sending to uninterested people (FP) wastes money. |
| **Credit Risk / Loan Default** | **ROC-AUC** | We want to assess how well the model separates risky from safe borrowers, across different thresholds. ROC-AUC gives a threshold-independent performance summary. |

📌 **Note:** Choose metrics based on **the cost of making wrong decisions** in your real-world use case.

---

## 🚀 Work on It

Clone the repo:  

git clone [https://github.com/imran-sony/classification-diabetes_detection.git](https://github.com/imran-sony/classification-diabetes_detection.git)  
cd classification-diabetes_detection


Run the notebook to train and evaluate models.
