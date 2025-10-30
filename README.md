# Task Manager ML System  
A machine-learning powered system for analysing and classifying tasks in a task-management workflow.

## 🎯 Project Overview  
This project loads historical task data (from CSV), preprocesses text fields, engineers features, and trains classification models (e.g., to predict task priority or category). It compares different feature-extraction techniques (TF-IDF vs word-embeddings) and multiple model types (Naive Bayes, SVM, Random Forest, XGBoost).  
The goal: help automate task classification, prioritisation or routing in a task-management context.

## 📂 Data & Preprocessing  
- The dataset is loaded from a CSV file (for example `GFG_FINAL.csv`).  
- Text columns are auto-detected (object type, average length >10).  
- Label/target columns are auto-detected (categorical with few unique values).  
- Text cleaning steps include: filling missing values, converting to lowercase, removing non-alphabetical characters, filtering out empty texts.  
- Two feature-extraction approaches:  
  1. **TF-IDF**: max_features=1000, min_df=2, max_df=0.8, ngram_range=(1,2), stop_words='english'.  
  2. **Word-Embeddings**: e.g., using Word2Vec to create dense document embeddings by averaging word vectors.

## 🧪 Model Training & Evaluation  
- Data split: 80% train / 20% test, stratified by target label, random_state=42.  
- Models trained/compared:  
  - MultinomialNB (Naive Bayes)  
  - SVC (Support Vector Machine)  
  - RandomForestClassifier (Random Forest)  
  - XGBClassifier (XGBoost)  
- Metrics reported: Accuracy, Precision, Recall, F1-score, Training time.  
- Comparative evaluation: TF-IDF features vs Word‐Embeddings features.

## ✅ Highlights & Findings  
- Produced clean text dataset and features ready for modelling.  
- Found which model/feature-extraction combo gave best accuracy for the task classification objective.  
- Provided a performance dashboard (bar charts, confusion matrix, detailed metrics) for comparison.  
- Made recommendations based on results (e.g., “If embeddings perform better, use them; else stick with TF-IDF for efficiency”).

## 🚀 Setup & Usage  
1. Clone the repository:  
   ```bash
   git clone <your-repo-url>
   cd <project-folder>

# 📊 AI-Powered Task Management System  
Comprehensive Visualisation & Analytics for Task Management Workflows

## 🧭 Project Overview  
This project analyses a task management dataset to provide insights and predictive capabilities.  
Key goals:  
- Load and inspect historic tasks (categories, priorities, statuses, timestamps)  
- Clean and preprocess textual and metadata features  
- Visualise distributions (category, priority, status) and temporal trends  
- Engineer features from text and metadata (e.g., task descriptions, assignees, time fields)  
- Compare feature-extraction methods (TF-IDF, embeddings) and train classification models  
- Generate dashboards and analytics of workload, task patterns & status interplay  
 
