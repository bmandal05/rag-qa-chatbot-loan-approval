# 🧠 RAG Q&A Chatbot for Loan Approval Dataset

This project implements a **Retrieval-Augmented Generation (RAG) based chatbot** that can answer natural language questions about loan approval cases using a Kaggle dataset.

It combines:
- 🔍 **Document retrieval** using FAISS and MiniLM embeddings
- 🤖 **Natural language generation** using Hugging Face's `flan-t5-small`
- 📊 **Structured data** from a real-world loan approval dataset

---

## 📂 Dataset

**Kaggle Loan Approval Dataset**  
📎 [Kaggle Link](https://www.kaggle.com/datasets/sonalisingh1411/loan-approval-prediction)

- Dataset: `Training Dataset.csv`
- Fields include: ApplicantIncome, Credit_History, Property_Area, Loan_Status, etc.

---

## ⚙️ How It Works

1. Each row in the dataset is converted into a plain text document.
2. Embeddings are generated using `all-MiniLM-L6-v2` from SentenceTransformers.
3. FAISS is used to retrieve the top relevant entries based on the user query.
4. A lightweight LLM (`flan-t5-small`) generates an answer using the context.

---

## 🚀 Run the Project in Google Colab

> Make sure you upload your `kaggle.json` file before downloading the dataset.

```bash
# Step 1: Install dependencies
!pip install sentence-transformers faiss-cpu transformers

# Step 2: Load the dataset using kagglehub or kaggle CLI

# Step 3: Run the embedding, retrieval, and generation pipeline
