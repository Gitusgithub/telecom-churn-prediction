# 🎯 Telecom Customer Churn Prediction  
### *Phase 3 Data Science Project*

---

## 📋 Project Overview
This project addresses a critical business challenge in the telecom industry: **customer churn**. By analyzing customer behavior patterns, we've built a machine learning model that identifies customers at risk of leaving 30-60 days before they cancel service, enabling proactive retention strategies.

**Key Achievement:** Our model achieves **86% accuracy** and identifies **79.5% of actual churners**, with potential annual savings of **$72,000-$96,000**.

---

## 🎯 Business Problem
### The Challenge
- **14.5% annual churn rate** (483 customers leaving yearly)
- **$500 average cost** per lost customer (acquisition + lost revenue)
- **$241,500 annual revenue at risk**
- **Current approach:** Reactive (respond to cancellation requests)

### The Solution
Transform from **reactive** to **proactive** customer retention by predicting churn before it happens.

---

## 📊 Dataset
**Source:** Telecom customer records  
**Size:** 3,333 customers with 21 features  
**Time Period:** 12 months of historical data

### Key Features:
- **Demographic:** Account length, area code
- **Service Plans:** International plan, voice mail plan
- **Usage Patterns:** Day/evening/night/international minutes
- **Customer Service:** Number of service calls
- **Target Variable:** `churn` (True/False)

---

## 🔬 Methodology
### 1. **Data Exploration & Preparation**
- Exploratory Data Analysis (EDA) with visualizations
- Handling multicollinearity (removed calculated charge columns)
- Feature engineering (created interaction features)
- Train/validation/test split (60%/20%/20%)

### 2. **Model Development** *(Iterative Approach)*
#### **Baseline Models:**
- **Dummy Classifier** (always predict majority class)
- **Logistic Regression** (interpretable baseline)

#### **Advanced Models:**
- **Decision Tree Classifier** (non-parametric)
- **Tuned Decision Tree** (hyperparameter optimization)
- **Random Forest** (ensemble method - selected as final model)

### 3. **Model Evaluation**
- **Primary Metric:** Recall (catch as many churners as possible)
- **Secondary Metrics:** Precision, F1-Score, AUC-ROC
- **Business-focused evaluation:** Cost-benefit analysis

---

## 📈 Results & Insights

### **Final Model Performance**
| Metric | Score | Business Interpretation |
|--------|-------|-------------------------|
| **Accuracy** | 85.7% | Overall correct prediction rate |
| **Recall** | 79.5% | Identifies 8 out of 10 actual churners |
| **Precision** | 63.8% | When flagged, 64% will actually churn |
| **F1-Score** | 70.8% | Balanced performance measure |
| **AUC-ROC** | 89.1% | Excellent discriminatory power |

### **Key Business Insights**
1. **Top Churn Drivers:**
   - **Customer service calls:** 4+ calls = 5× higher churn risk
   - **International plans:** 42% churn rate vs 11% for domestic-only
   - **Daytime usage:** High usage correlates with churn

2. **Protective Factors:**
   - **Voice mail subscribers:** 50% less likely to churn
   - **Evening usage:** Slight protective effect

### **Financial Impact**
- **Potential annual savings:** $72,000 - $96,000
- **ROI on retention spending:** ~300%
- **30% churn reduction** achievable within 6 months

---

## 🚀 How to Run This Project

### **Prerequisites**
- Python 3.8+
- Jupyter Notebook
- Git (for cloning)

### **Installation**
```bash
# 1. Clone the repository
git clone https://github.com/YOUR-USERNAME/telecom-churn-prediction.git

# 2. Navigate to project directory
cd telecom-churn-prediction

# 3. Install dependencies
pip install -r requirements.txt