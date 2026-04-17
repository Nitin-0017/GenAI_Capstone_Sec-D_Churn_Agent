# Customer Churn Prediction with AI Agent

An end-to-end Machine Learning and AI Agent system that predicts customer churn and generates actionable business recommendations using Retrieval-Augmented Generation (RAG) and Large Language Models (LLMs).

---

## Project Overview

This project addresses a critical business problem: predicting whether a customer will churn.

The system goes beyond traditional machine learning by:

- Predicting churn probability  
- Explaining the reason behind predictions  
- Retrieving relevant behavioral insights  
- Generating human-like retention strategies  

This transforms a predictive model into a decision-support AI system.

---

## Key Features

- Churn prediction using machine learning models  
- Complete preprocessing pipeline (encoding and scaling)  
- Threshold tuning (0.85) for business optimization  
- AI Agent with multi-step reasoning  
- RAG using ChromaDB vector database  
- LLM-based recommendations using Groq (LLaMA 3.1)  
- Model evaluation using accuracy, precision, recall, and F1 score  

---

## System Flow

User Input → Data Preprocessing → ML Model → Query Generator → RAG → LLM → Final Output

---

## Agent Architecture

The system uses a multi-step AI Agent pipeline:

- Predict Node: Generates churn prediction and probability using ML model  
- RAG Node: Retrieves relevant insights using vector similarity search  
- Advice Node: Uses LLM to generate reasoning, risk level, and retention strategy  

This design ensures the system is explainable and actionable.

---

## Dataset

- Source: Kaggle Customer Churn Dataset  
- Records: 440,832  
- Features: 11  
- Target: Churn (0 = No, 1 = Yes)

### Key Features

- Age  
- Tenure  
- Usage Frequency  
- Support Calls  
- Payment Delay  
- Subscription Type  
- Contract Length  
- Total Spend  

---

## Models Used

| Model               | Accuracy | Precision | Recall | F1 Score |
|--------------------|----------|----------|--------|----------|
| Logistic Regression | 0.63     | 0.56     | 0.93   | 0.70     |
| Random Forest      | 0.52     | 0.49     | 0.99   | 0.66     |
| Decision Tree      | 0.51     | 0.49     | 0.99   | 0.65     |

Final Model: Logistic Regression (Threshold = 0.85)

---

## Threshold Strategy

Instead of using the default threshold of 0.5, a threshold of 0.85 was selected to:

- Reduce false positives  
- Focus on high-risk customers  
- Improve decision-making reliability  
- Optimize F1 score  

---

## Sample Output

Prediction: Churn  
Probability: 0.99  
Risk Level: High  

Insights:
- High support calls  
- Low tenure  
- Payment delays  

Recommendation:
Offer discounts, improve support, and increase engagement  

---

## Tech Stack

### Machine Learning
- Python  
- scikit-learn  
- Pandas  
- NumPy  

### AI Agent
- LangGraph  
- LangChain  
- ChromaDB  
- HuggingFace Embeddings  
- Groq API (LLaMA 3.1)  

### Tools
- Streamlit  
- joblib  

---

## How to Run

git clone https://github.com/your-username/churn-agent.git  
cd churn-agent  
pip install -r requirements.txt  
streamlit run app.py  

---

## Project Structure

├── data/  
├── notebook/  
├── model/  
│   └── full_pipeline.pkl  
├── agent/  
├── app/  
│   └── app.py  
├── report/  
├── requirements.txt  
└── README.md  

---

## Key Learnings

- Importance of balancing precision and recall  
- Impact of threshold tuning on business outcomes  
- Use of RAG to improve LLM reliability  
- Building modular AI agent pipelines  
- Prompt engineering for controlled outputs  

---

## Limitations

- Limited RAG knowledge base  
- No cross-validation  
- No time-series behavioral data  
- Linear pipeline without advanced branching  

---

## Team

- Kartik Yadav – Model Training, RAG, Report  
- Nitin Kumar – Evaluation, Streamlit, LangGraph Agent  
- Prateek Shakya – Data Processing, LLM Setup  

---

## License

This project is for academic and learning purposes.
