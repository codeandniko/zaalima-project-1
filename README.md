# 🧠 Task Manager ML System  
A machine-learning powered system for analysing and classifying tasks in a task-management workflow.

---

## 🎯 Project Overview  
This project loads historical task data (from CSV), preprocesses text fields, engineers features, and trains classification models (e.g., to predict task priority or category).  
It compares different feature-extraction techniques (**TF-IDF** vs **Word Embeddings**) and multiple model types (**Naive Bayes**, **SVM**, **Random Forest**, **XGBoost**).  
The goal: help automate task classification, prioritisation or routing in a task-management context.

---

## 📂 Data & Preprocessing  
- Dataset: CSV input (e.g., `GFG_FINAL.csv`)  
- Automatic detection:
  - **Text Columns:** `dtype=object`, average length >10  
  - **Label Columns:** Categorical with few unique values  
- Text cleaning:
  - Fill missing values  
  - Convert to lowercase  
  - Remove non-alphabetic characters  
  - Filter empty strings  
- Feature Extraction:
  1. **TF-IDF:** `max_features=1000`, `min_df=2`, `max_df=0.8`, `ngram_range=(1,2)`, `stop_words='english'`
  2. **Word Embeddings:** Dense representations using averaged Word2Vec embeddings  

---

## 🧪 Model Training & Evaluation  
- **Data Split:** 80% train / 20% test (stratified, `random_state=42`)  
- **Models Tested:**  
  - MultinomialNB (Naive Bayes)  
  - SVC (Support Vector Machine)  
  - RandomForestClassifier  
  - XGBClassifier  
- **Metrics:** Accuracy, Precision, Recall, F1-score, Training time  
- **Comparison:** Each model trained on both TF-IDF and Embedding features  

---

## 📊 Feature Extraction Comparison  

Below is a sample comparison result generated during experiments:  

![Feature Extraction Comparison]<img width="1259" height="271" alt="image" src="https://github.com/user-attachments/assets/ef743858-b061-497b-a946-e8e3e561e51f" />


**Performance Summary:**  
- 🥇 **Best Overall:** XGBoost  
- 📈 **Best Accuracy:** 0.9959  

---

## 🖼️ User Interface & Visualization  
<img width="1902" height="861" alt="image" src="https://github.com/user-attachments/assets/892338f8-d7d6-4196-9547-0674316c6079" />
<img width="1881" height="910" alt="image" src="https://github.com/user-attachments/assets/e2ed1459-b359-4466-b507-1af7e2a2f45b" />

### 📌 Dashboard – Task Overview  
<img width="1191" height="944" alt="image" src="https://github.com/user-attachments/assets/39f7c500-fe61-4b9c-929e-d6ff85d81ce3" />
 

---

## ✅ Highlights & Findings  
- Preprocessed and vectorized text data efficiently  
- Compared model and feature extraction combinations  
- Identified best configuration for classification accuracy  
- Produced interpretable visualizations and analytics dashboards  
- Generated recommendations for deployment-ready models  

---

## 🚀 Setup & Usage  

```bash
# 1. Clone the repository
git clone <your-repo-url>
cd <project-folder>

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the main script
python main.py



