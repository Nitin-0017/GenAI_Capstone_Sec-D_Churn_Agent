# 📊 Customer Churn Prediction with AI Agent

An end-to-end **Machine Learning + AI Agent system** that predicts customer churn and generates **actionable business recommendations** using Retrieval-Augmented Generation (RAG) and LLMs.

---

## 🚀 Project Overview

This project solves a critical business problem:  
👉 **Predicting whether a customer will churn (leave the service)**

It combines:
- Traditional **Machine Learning models**
- A **custom threshold optimization strategy**
- An advanced **AI Agent system (LangGraph + RAG + LLM)**

The system not only predicts churn but also:
- Explains *why* a customer may churn  
- Retrieves domain knowledge  
- Generates **human-like retention strategies**

---

## 🧠 Key Features

- 📈 Churn Prediction using ML models  
- ⚙️ Full preprocessing pipeline (cleaning, encoding, scaling)  
- 🎯 Threshold tuning (0.85) for business optimization  
- 🤖 AI Agent with multi-step reasoning  
- 🔍 RAG (Retrieval-Augmented Generation) using ChromaDB  
- 💬 LLM-based recommendation system (Groq – LLaMA 3.1)  
- 📊 Model evaluation with Accuracy, Precision, Recall, F1  

---

## 🏗️ System Architecture


Raw Customer Data
↓
[ Predict Node (ML Model) ]
↓
[ RAG Node (Knowledge Retrieval) ]
↓
[ Advice Node (LLM Recommendation) ]
↓
Final Output (Prediction + Insights + Strategy)


---

## 📂 Dataset

- Source: Kaggle Customer Churn Dataset  
- Total Records: **440,832**  
- Features: **11**  
- Target: **Churn (0 = No, 1 = Yes)**  

### Important Features:
- Age  
- Tenure  
- Usage Frequency  
- Support Calls  
- Payment Delay  
- Subscription Type  
- Contract Length  
- Total Spend  

---

## ⚙️ Tech Stack

### 🔹 Machine Learning
- Python  
- scikit-learn  
- Pandas, NumPy  

### 🔹 AI Agent
- LangGraph  
- LangChain  
- ChromaDB (Vector DB)  
- Groq (LLaMA 3.1-8b-instant)  

### 🔹 Tools
- joblib (model serialization)  
- Matplotlib / Seaborn  

---

## 📊 Models Used

| Model               | Accuracy | Precision | Recall | F1 Score |
|--------------------|----------|----------|--------|----------|
| Logistic Regression (Final) | 0.63 | 0.56 | 0.93 | 0.70 |
| Random Forest      | 0.52 | 0.49 | 0.99 | 0.66 |
| Decision Tree      | 0.51 | 0.49 | 0.99 | 0.65 |

👉 **Final Model: Logistic Regression (Threshold = 0.85)**

---

## 🎯 Why Threshold = 0.85?

Instead of default 0.5:
- Reduces **false positives**
- Focuses on **high-risk customers**
- Optimizes **F1 Score**
- Saves business cost on unnecessary retention offers

---

## 🤖 AI Agent Workflow

### 1️⃣ Prediction Node
- Takes customer data  
- Outputs churn probability + prediction  

### 2️⃣ RAG Node
- Retrieves relevant churn insights  
- Uses ChromaDB vector search  

### 3️⃣ Advice Node
- Uses LLM to generate:
  - Reason  
  - Risk Level (Low / Medium / High)  
  - Retention Strategy  

---

## 📌 Sample Output


Prediction: Churn
Probability: 0.99
Risk Level: High

Insights:

High support calls
Low tenure
Payment delays

Recommendation:
Offer discounts, upgrade plan, assign dedicated support.


---

## 📁 Project Structure

├── data/
│   ├── training.csv
│   ├── testing.csv
│
├── notebook/
│   └── churn_model.ipynb
│
├── model/
│   └── full_pipeline.pkl
│
├── agent/
│   ├── predict_node.py
│   ├── rag_node.py
│   ├── advice_node.py
│
├── app/
│   └── streamlit_app.py
│
├── report/
│   └── project_report.pdf
│
└── README.md

## 🧪 Key Learnings

- Real-world ML is about **trade-offs (precision vs recall)**  
- Threshold tuning is sometimes **more important than model choice**  
- AI Agents can turn ML models into **decision-making systems**  
- RAG improves LLM **reliability and relevance**  

---

## ⚠️ Limitations

- Small RAG knowledge base  
- No cross-validation  
- Limited features (no behavioral time-series data)  
- Linear agent pipeline (no branching logic)  

---

## 🔮 Future Improvements

- Add XGBoost / LightGBM  
- Expand RAG knowledge base  
- Build REST API (FastAPI)  
- Add real-time dashboard  
- Use time-series features  
- Implement smarter agent routing  

---

## 👥 Team

- **Kartik Yadav** – Preprocessing, Report  
- **Nitin Kumar** – Model Training, Evaluation, Streamlit  
- **Prateek Shakya** – Data, Streamlit  

---

## 📜 License

This project is for academic and learning purposes.
