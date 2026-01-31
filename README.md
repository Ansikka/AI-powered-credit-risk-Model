# AI-Powered Credit Risk Modeling with GenAI 

📌 Project Overview

This project implements an end-to-end Credit Risk Modeling pipeline to estimate the Probability of Default (PD) for consumer loans and extends it with a GenAI-powered Decision Intelligence layer using Retrieval-Augmented Generation (RAG).

The system not only predicts credit risk using machine learning models but also explains underwriting decisions by retrieving internal credit policies and risk documentation, enabling interpretable and policy-aligned loan decisions.

🏦 Business Context

In consumer lending, incorrect risk assessment can lead to:

High default rates (financial loss)
Over-strict rejection (lost revenue)
This project addresses both by:
Optimizing recall to correctly identify risky customers
Translating ML outputs into business-understandable explanations

🧠 System Architecture

Customer Data
   ↓
ML Risk Model (PD Prediction)
   ↓
Expected Loss Calculation
   ↓
Approval / Rejection Decision
   ↓
GenAI RAG Assistant
   ↓
Human-Readable Risk Explanation

🔍 Machine Learning Component
Models Implemented

Logistic Regression (baseline, industry standard)

XGBoost Classifier (non-linear, high performance)

Key Features

Feature preprocessing & scaling

ROC-AUC based model comparison

Confusion Matrix & Recall analysis

Probability calibration for risk scores

Why Recall Matters

In loan default prediction:

False Negatives (missed defaulters) are more costly than false positives

High recall ensures risky borrowers are correctly identified

📊 Risk Metrics Used

Probability of Default (PD)

Expected Loss (EL)

𝐸
𝐿
=
𝑃
𝐷
×
𝐿
𝐺
𝐷
×
𝐸
𝐴
𝐷
EL=PD×LGD×EAD

These metrics directly support portfolio-level decision making.

🤖 GenAI / LLM Component (RAG)
What Was Built

A GenAI-powered Risk & Policy Assistant using Retrieval-Augmented Generation (RAG).

Why RAG?

Avoids hallucination

Grounds LLM responses in internal credit policy documents

Enables explainable, auditable AI decisions (critical in fintech)

Knowledge Base

Stored in the docs/ folder:

Credit approval rules

PD thresholds

Expected Loss explanations

Example Questions the AI Can Answer

Why was this loan rejected?

What does a PD of 12% indicate?

How does Expected Loss affect approval decisions?

Why is recall important in credit risk modeling?

🧩 GenAI Workflow
User Query
   ↓
Text Embeddings
   ↓
Vector Database (FAISS)
   ↓
Relevant Policy Retrieval
   ↓
LLM Generates Grounded Explanation

📂 Project Structure

AI-powered-credit-risk-Model/

│

├── loan_project.ipynb              # ML credit risk pipeline

├── genai_risk_assistant.ipynb      # RAG-based GenAI assistant

├── cr_loan.csv                     # Dataset

│

├── docs/                           # Knowledge base

│   ├── credit_policy.txt

│   ├── risk_thresholds.txt

│   ├── expected_loss_explained.txt

│

├── ROC_curve.png

├── XGBoost_confusion_matrix.png

├── README.md

🛠 Tech Stack

Machine Learning

Python, Pandas, NumPy

Scikit-learn

XGBoost

GenAI / LLM

LangChain

OpenAI / Embeddings

FAISS (Vector Store)

Evaluation

ROC-AUC

Recall, Precision

Confusion Matrix

Probability Calibration

🚀 Key Outcomes

Built a production-style credit risk model

Integrated GenAI for explainable underwriting

Demonstrated ML + business + AI alignment

Designed an intern-level yet industry-relevant RAG system
