# Credit Risk Modeling Project  

This project focuses on building a **Credit Risk Model** to predict the likelihood of loan default. The objective is to assist the Risk Unit in identifying potential defaulters while minimizing missed defaults by maximizing recall.  
The model is designed as a binary classification system (1 = Default, 0 = Non-default), leveraging customer demographics, loan details, and credit bureau data to provide accurate predictions. An interactive **Streamlit** application allows users to input customer details and receive real-time credit risk predictions, enabling data-driven decision-making.  

## Key Features  

1. **Data Preprocessing**:  
   - Missing value imputation and feature scaling using *Min-Max Scaling*.  
   - Feature selection through **Information Value (IV)** and **Variance Inflation Factor (VIF)** to remove multicollinear features.  

2. **Exploratory Data Analysis (EDA)**:  
   - Insights into key predictors like income stability, credit utilization ratio, delinquency history, and loan-to-income (LTI) ratio.  
   - Analysis of secured vs. unsecured loan default rates.  

3. **Class Imbalance Handling**:  
   - Addressed significant imbalance (80% non-defaulters vs. 20% defaulters).  
   - Explored undersampling, oversampling, and *SMOTE-Tomek* techniques.  

4. **Model Development**:  
   - Evaluated Logistic Regression, Random Forest, and XGBoost models.  
   - Logistic Regression was finalized for its high recall in identifying defaulters.  

5. **Hyperparameter Tuning**:  
   - Optimized Logistic Regression using **Optuna** for enhanced performance.  

6. **Interactive Web Application**:  
   - Built using **Streamlit** for real-time predictions.  
   - User-friendly interface for inputting customer data like income, loan amount, and credit utilization.  

## Tools and Technologies  

- **Languages**: Python  
- **Libraries**:  
  - Data Processing: `pandas`, `numpy`  
  - Visualization: `matplotlib`, `seaborn`  
  - Imbalance Handling: `imblearn` (SMOTE-Tomek)  
  - Machine Learning: `scikit-learn`, `xgboost`  
  - Hyperparameter Tuning: `optuna`  
- **Framework**: Streamlit  
- **Dataset**: 50,000 loan records (Feb 2022 - Feb 2024)  

## Project Highlights  

- **Handling Class Imbalance**:  
   - Baseline models were evaluated without balancing to understand limitations.  
   - *SMOTE-Tomek* effectively balanced the dataset without losing critical information.  

- **Model Performance**:  
   - Logistic Regression achieved the best recall for defaulters.  
   - Final model balances high recall and robustness, avoiding overfitting.  

- **Business Insights**:  
   - Higher credit utilization, longer loan tenures, and delinquency history strongly correlate with defaults.  
   - Secured loans exhibit lower default rates compared to unsecured loans.  

## Installation and Usage  

### Prerequisites  
- Python 3.8+  
- pip  

### Steps  

1. Clone the repository:  
   ```bash  
   git clone https://github.com/manideepcheekoti/ml-project-credit-risk-model.git  
   cd ml-project-credit-risk-model  
   ```  

2. Install the required dependencies:  
   ```bash  
   pip install -r requirements.txt  
   ```  

3. Run the Streamlit application:  
   ```bash  
   streamlit run app.py  
   ```  

4. Open the app in your browser at: `http://localhost:8501`  

---

## Results  

- **Class Imbalance Handling**: *SMOTE-Tomek* improved recall for defaulters from ~50% to ~90%.  
- **Final Model**: Logistic Regression achieved a high recall and robust performance.  
- **Interactive App**: Simplified credit risk assessment.  

---

## Future Enhancements  

- Integrate user authentication for secure access.  
- Include time-series visualizations for historical trend analysis.  
- Extend model capabilities to support multi-class risk segmentation.  

---

## Demo  

Try the live application here: [Credit Risk Model App](https://ml-project-credit-risk-score-model.streamlit.app/)  

For a detailed walkthrough, visit the project repository: [GitHub Repository](https://github.com/manideepcheekoti/ml-project-credit-risk-model)  

---  







