# Readmission Prediction Project

### Overview
This project focuses on predicting patient readmission within 30 days using clinical data. Hospital readmissions can indicate poor patient outcomes and contribute to increased healthcare costs. By leveraging machine learning techniques, this project aims to identify key factors associated with readmissions and build a predictive model that can assist healthcare professionals in making data-driven decisions.

### Data Sources
The dataset consists of multiple healthcare-related files, including patient demographics, hospital admissions, diagnoses, laboratory test results, procedures, and medical history. The key datasets used in this project include:
- **Admissions Data:** Contains information about hospital admissions, including admission type, discharge time, and patient identifiers.
- **Diagnoses Data:** Includes ICD-9 codes for diseases diagnosed during the hospital stay.
- **Lab Events Data:** Stores laboratory test results recorded during the hospital stay.
- **Patient Demographics:** Provides essential details such as age, ethnicity, and marital status.
- **Procedures Data:** Contains information about medical procedures performed during the hospital stay.

### Data Processing
1. **Identifying Heart Failure Patients**
   - Specific ICD-9 codes were used to flag patients diagnosed with heart failure.
2. **Processing Lab Events Data**
   - Laboratory test results were aggregated at the admission level by computing the average lab value.
3. **Merging Data**
   - Various datasets were merged to create a unified dataset containing comprehensive patient information.
4. **Feature Engineering**
   - Readmission was defined as a hospital return within 30 days of discharge.
   - New features such as average lab value were derived to improve predictive power.
5. **Data Cleaning & Outlier Removal**
   - Missing values were handled, and extreme values were removed using the interquartile range (IQR) method.

### Machine Learning Workflow
1. **Feature Selection**
   - Relevant features such as admission type, insurance, marital status, ethnicity, heart failure diagnosis, and lab values were chosen.
2. **Encoding Categorical Variables**
   - Categorical attributes were transformed using label encoding to make them compatible with machine learning models.
3. **Data Splitting**
   - The dataset was divided into training and testing sets (80-20 split) to evaluate model performance.
4. **Handling Class Imbalance**
   - Since readmission cases are often imbalanced, downsampling was applied to create a balanced dataset.
5. **Feature Standardization**
   - StandardScaler was used to normalize features to improve model efficiency.
6. **Model Training**
   - A **Random Forest Classifier** was trained with hyperparameter tuning using GridSearchCV to optimize performance.
7. **Evaluation**
   - The model's accuracy, precision, recall, F1-score, and confusion matrix were analyzed to assess its predictive ability.

### Results
- The model achieved an accuracy of **83%**.
- High recall for the readmitted class (99%) ensures that most patients at risk of readmission are identified.
- The confusion matrix indicates strong performance, but some false positives and false negatives remain.

### Conclusion
This project demonstrates how machine learning can be utilized to predict hospital readmissions, aiding healthcare providers in proactive decision-making. Future improvements could involve using deep learning models, incorporating additional clinical variables, and refining feature engineering techniques. The insights gained from this study can contribute to reducing readmission rates and improving patient care outcomes.

