# Health Insurance Project
Project Overview: Health Insurance Charges Prediction.

Created by Lucy Hill.

The primary goal of this project is to develop a predictive model that estimates health insurance charges based on various factors, including demographics and the presence of existing medical condition. 
By leveraging this information, we can use this so that insurance companies can set premiums more accurately and manage risk effectively.

Throughout this project, we focused on several key skills, including:

•	**Data Preprocessing**: Cleaning and preparing the dataset for analysis.

•	**Exploratory Data Analysis (EDA)**: Investigating the dataset to identify trends and patterns.

•	**Machine Learning**: Applying algorithms to develop the predictive model.

•	**Feature Engineering**: Creating new features to improve model performance.

•	**Model Evaluation**: Assessing the model’s accuracy and reliability using various metrics.

**Data Description**

We used real-world data from the Data Source: https://www.kaggle.com/datasets/mirichoi0218/insurance.

| Column   | Description                                                                                          |
|----------|------------------------------------------------------------------------------------------------------|
| age      | Age of primary beneficiary                                                                           |
| sex      | Insurance contractor gender (female, male)                                                          |
| bmi      | Body mass index, providing an understanding of body weights that are relatively high or low relative to height |
| children | Number of children covered by health insurance                                                       |
| smoker   | Smoking status                                                                                      |
| region   | The beneficiary’s residential area in the US (northeast, southeast, southwest, northwest)          |
| charges  | Individual medical costs billed by health insurance                                                  |

In this project, we introduced a new column, existing_medical_conditions, to the dataset to analyse its impact on health insurance charges. 
This variable was randomly assigned to various customers, allowing us to explore whether having an existing medical condition, alongside being a smoker and having a BMI over 30, significantly affects insurance charges. 
By comparing high-risk customers (smokers with a BMI over 30) to those with existing medical conditions and those without, we can determine if the presence of these conditions correlates with higher insurance costs.

**Exploratory Data Analysis (EDA)**:

![Untitled](https://github.com/user-attachments/assets/7329daa9-cd2e-4c47-8489-e5ad3efae596)
![Untitled](https://github.com/user-attachments/assets/cb7bbeaf-b8fb-4d68-961a-b13b9237a452)
![Untitled](https://github.com/user-attachments/assets/5caef249-6ee5-4174-ac04-14a4efb796a9)
![Untitled](https://github.com/user-attachments/assets/3d9e61fa-4be5-42fb-9325-1ef0bad6c5a5)


What we have gathered from the Exploratory Data Analysis (EDA) is the following insights: 
Most people in this data set are non-smokers and are obese. 
The comparison of charges by age for smokers and non-smokers shows a significant trend, that is non-smokers tend to have lower insurance charges across all age groups. While smokers automatically face higher charges, regardless of age.

The average insurance charges for smoking status are $32,050.23 for smokers, whereas for non-smokers the average is significantly lower at $8,434.27.

Furthermore, the average charges based on existing medical conditions indicate that individuals without any medical conditions incur average charges of $12,733.10, while those with existing medical conditions face higher average charges of $15,347.40.

**Data Processing**

**Missing Values**: No missing values were found in the dataset.

**Duplicate Rows**: Identified and removed any duplicate rows in the data.

**Categorical Encoding**: Used One-Hot Encoding for categorical variables like gender, smoker status, region to convert them into numerical form for modelling.

**Modelling**: Performed a train-test split, evaluated different algorithms such as Linear Regression, Random Forest and lastly fine tuning hyperparameters.

**Feature Engineering**: Added a new column for existing medical conditions to the dataset.

**Model Evaluation**
| Metric    | Linear Regression | Random Forest |
|-----------|-------------------|---------------|
| R²        | 0.78              | 0.87          |
| MAE       | 4198.24           | 2566.10       |


**Conclusion** 

In this project, we analysed how different factors, including age, smoking status, and existing medical conditions, influence insurance charges.

Through our findings we found that smokers incur significantly higher average insurance charges ($32,050.23) compared to non-smokers ($8,434.27), highlighting the significant impact of smoking on insurance costs. 

Additionally, individuals with existing medical conditions face higher charges ($15,347.40) than those without ($12,733.10).

These results highlight the significant role that smoking status and existing medical conditions have on insurance charges, for risk assessments and pricing strategies.

We also built and evaluated regression models to predict insurance charges, achieving an R² score of 0.88 in both scenarios. 
While the models demonstrated good predictive performance, residual analysis indicated that they tended to underpredict higher charges, especially in mid-range values. 
Suggested areas for improvement are hyperparameter optimization and feature engineering.
