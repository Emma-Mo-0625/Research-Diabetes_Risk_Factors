# 📊 Diabetes Risk Analysis Using Health Indicators

## 🏥 UCLA Biostat 203A - Master in Data Science in Health

### 👩‍🔬 **Author**: Rongrong (Emma) Mo  
### 🎓 **Institution**: UCLA Fielding School of Public Health  
### 📅 **Semester**: Fall 2024  

---

## 📌 **Project Overview**
Diabetes is a major public health challenge, affecting millions globally and significantly impacting healthcare systems. This study investigates how **physical health, mental health, smoking, and physical activity** influence diabetes risk using data from the **Behavioral Risk Factor Surveillance System (BRFSS) 2015**. 

By employing **logistic regression** and **hypothesis testing**, we analyze key lifestyle and health-related factors to determine their predictive power in identifying diabetes. The findings aim to contribute to **early detection, prevention, and intervention strategies** for diabetes management.

---

## 📂 **Dataset**
- **Name**: [Diabetes Health Indicators Dataset](https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset)
- **File Used**: `diabetes_binary_5050split_health_indicators_BRFSS2015.csv`
- **Source**: Kaggle - Derived from **CDC BRFSS**  
- **Size**: 70,692 participants (Balanced dataset: 50% Diabetic, 50% Non-Diabetic)
- **Features Used**:
  - **Mental Health**: Number of poor mental health days in the last 30 days
  - **Physical Health**: Number of poor physical health days in the last 30 days
  - **Smoking**: Binary (Smoker/Non-Smoker)
  - **Physical Activity**: Binary (Active/Inactive)
  - **Diabetes Status**: Binary outcome (Diabetes/No Diabetes)

---

## 📊 **Methodology**
### 🧪 **Statistical Analysis & Modeling**
1. **Data Preprocessing**
   - Handled missing values and verified variable distributions.
   - Applied **descriptive statistics** to understand dataset characteristics.

2. **Hypothesis Testing**
   - **Welch’s t-tests**: Compared mental and physical health between diabetic and non-diabetic groups.
   - **Chi-square tests**: Assessed relationships between diabetes status and categorical predictors.

3. **Correlation Analysis**
   - Explored associations between **mental health and physical health**.

4. **Logistic Regression**
   - Built a predictive model using **physical health, mental health, smoking, and physical activity**.
   - Evaluated variable significance and model coefficients.

5. **Model Evaluation**
   - Used **confusion matrix**, **ROC curve**, and **AUC score** to assess predictive performance.
   - Splitted data into **50% training, 50% testing** to validate model effectiveness.

---

## 📈 **Key Findings**
### 🔬 **Hypothesis Testing Results**
- Diabetic individuals report significantly **more poor physical health days** (**7.95 days** vs. **3.67 days**, p < 2.2e-16).
- Mental health days also differ significantly (**4.46 days** vs. **3.04 days**, p < 2.2e-16), but logistic regression suggests its effect is minor.
- Smoking is **positively associated** with diabetes (51.8% in diabetic group vs. 43.2% in non-diabetic, p < 2.2e-16).
- **Physical activity is negatively associated** with diabetes (**63.1% active in diabetic group vs. 77.6% in non-diabetic**, p < 2.2e-16).

### 🤖 **Logistic Regression Insights**
| Predictor        | Coefficient (Log-Odds) | Odds Ratio | p-value | Impact |
|-----------------|----------------------|-----------|---------|--------|
| **Physical Health**  | +0.04   | 1.041  | < 0.001 | 📈 Positive |
| **Smoking**         | +0.219  | 1.244  | < 0.001 | 📈 Positive |
| **Physical Activity** | -0.524  | 0.592  | < 0.001 | 📉 Negative |
| **Mental Health**   | ~0.00   | 1.00   | 0.7875  | ❌ Not Significant |

### 📊 **Model Performance**
- **Accuracy**: **60.6%**
- **Sensitivity (Recall)**: **51.5%** (Limited ability to detect diabetic cases)
- **Specificity**: **69.6%** (Better at identifying non-diabetic individuals)
- **AUC (Area Under Curve)**: **0.6468** (Moderate predictive ability)

---

## 🔍 **Conclusions**
- **Physical health and smoking** significantly increase diabetes risk.
- **Physical activity** plays a crucial role in **reducing** diabetes risk.
- **Mental health** shows a statistical association but is **not a strong predictor** when adjusted for other factors.
- The logistic regression model provides **moderate predictive performance** but has **low sensitivity**, missing many diabetic cases.
- Future work could **include more features (e.g., diet, socioeconomic status, family history)** and **improve model sensitivity** by tuning classification thresholds.

---

## 🛠 **Tools & Libraries Used**
- **Programming Language**: `R 4.4.1`
- **Libraries**:
  - `dplyr`, `ggplot2` - Data manipulation & visualization
  - `pROC` - ROC curve & AUC analysis
  - `caret` - Model evaluation
- **IDE**: RStudio  

---

## 📌 **Future Improvements**
✅ Fine-tuning classification thresholds to enhance sensitivity.  
✅ Exploring **machine learning models (Random Forest, XGBoost)** for improved predictions.  
✅ Incorporating **dietary, socioeconomic, and genetic** factors for better risk assessment.  
✅ Expanding analysis to **longitudinal data** to assess cause-effect relationships.

---

## 📜 **References**
1. **World Health Organization** (2024). *Diabetes - Fact Sheet*. [WHO Website](https://www.who.int/news-room/fact-sheets/detail/diabetes)
2. **CDC BRFSS** (2015). *Behavioral Risk Factor Surveillance System Survey Data*. [CDC Website](https://www.cdc.gov/brfss/index.html)
3. **Kaggle Dataset**: [Diabetes Health Indicators](https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset)

---

## 📧 **Contact**
📩 Email: `rongrongmo0625@g.ucla.edu`  
📍 UCLA Fielding School of Public Health  

🚀 *This project was developed as part of the Master in Data Science in Health program at UCLA, Fall 2024.*
