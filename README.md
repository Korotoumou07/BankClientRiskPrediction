## Bank Client Analysis: Predicting Good and Bad Clients

### Project Objective
Predict good and bad clients for an American bank to assess risk and support decision-making for loans and financial services.



### Project Description
This project analyzes the customer data of an American bank and builds Machine Learning models to identify:  
- Reliable clients (good clients, Y=1)  
- High-risk clients (bad clients, Y=0)  

The project follows a full workflow, including:  
1. **Feature Engineering**: data cleaning, categorical encoding, normalization, and class balancing (SMOTE).  
2. **Descriptive Analysis**: statistics, visualizations, and correlations to identify influential variables.  
3. **Modeling**: comparison of models (Logistic Regression, Random Forest) and combination to improve performance.  
4. **Recommendations**: actionable strategies to target and retain good clients.



### Technologies Used
- **Python**: analysis and modeling  
- **Jupyter Notebook**: interactive development  
- **Pandas, NumPy**: data manipulation and analysis  
- **Scikit-Learn, imbalanced-learn, XGBoost**: Machine Learning models and class imbalance handling  
- **Matplotlib, Seaborn**: data visualization  



### Project Workflow
#### 1. Feature Engineering
- Initial inspection: 21 columns, 41,176 rows after removing 12 duplicates.  
- Categorical encoding using `LabelEncoder`.  
- Normalization of numerical features with `StandardScaler`.  
- Class balancing with SMOTE for the target variable `y`.  
- Saved cleaned dataset (`banking_cleaned.csv`).  

#### 2. Descriptive Analysis
- Studied demographic, financial, and behavioral variables.  
- Visualizations: histograms, bar plots, boxplots, heatmaps.  
- Key variables correlated with target: `duration`, `previous`, `poutcome`.  

#### 3. Model Selection
- **Linear Regression**: not suitable for binary classification.  
- **Logistic Regression**: simple, interpretable, and handles class imbalance with `class_weight='balanced'`.  
- **Random Forest**: captures complex relationships, robust to class imbalance.  
- **Combined Model**: averaging predictions from Logistic Regression and Random Forest to improve detection of good clients.  

#### 4. Modeling and Results
- **Logistic Regression**: Y=1 recall = 87%, F1-score = 58%.  
- **Random Forest**: Y=1 recall = 46%, F1-score = 54%.  
- **Combined Model**: Y=1 recall = 76%, F1-score = 64%, AUC = 0.95.  

#### 5. Recommendations
- Train bank advisors to have longer, quality interactions (`duration`).  
- Target high-potential clients (`job`, `education`).  
- Re-engage previous clients with positive history (`poutcome`).  
- Personalize products based on financial preferences (`housing`, `loan`, `default`).  
- Optimize campaign timing (`month`, `day_of_week`).  

### Author
**Korotoumou COULIBALY**  
L3-MAIE, ISM Digital Campus  
Email: korotoumou.coulibaly1@ism.edu.sn  

