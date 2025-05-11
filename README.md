# Prediction-of-Diabetes: A-Machine-Learning-approach-using-Logistic-Regression-and-Decision-Trees
This project explores chronic disease risk factors by analyzing behavioral and demographic health indicators to predict diabetes likelihood. The analysis is based on real-world survey data collected by the CDC and includes both exploratory data analysis and predictive modeling using R.  

## Notes  
This project was developed using R in a local academic environment. While the dataset had to be downsampled to maintain class balance, the pipeline is fully functional and ready to scale. Interpretations were validated against statistical significance and domain knowledge.  

## Project Overview
Diabetes remains a pressing public health issue, with many individuals unaware of their risk status. Using CDC's BRFSS dataset, we applied statistical and machine learning models to identify key drivers of diabetes and evaluate predictive accuracy across a balanced sample.  

## Dataset  
- Source: Behavioral Risk Factor Surveillance System (BRFSS) by CDC
- Size: ~250,000 records before cleaning; reduced to ~70,000 for modeling
- Target Variable: Binary classification — Diabetic vs. Non-Diabetic

## Technologies Used  
- R (rpart, caret, ggplot2)
- Logistic Regression & Decision Trees
- Data Preprocessing & Visualization

## Key Features  
- Cleaned and downsampled a large real-world dataset to handle class imbalance
- Reclassified variables and engineered age buckets for better model interpretability
- Visualized relationships between BMI, blood pressure, age, and diabetes prevalence
- Built and pruned decision trees to address overfitting and improve model clarity
- Applied logistic regression to identify statistically significant predictors

## Notable Findings
### From Logistic Regression:  
- Individuals with High Blood Pressure have a 108% higher chance of developing diabetes.
- Having High Cholesterol increases the odds by 82%.
- A history of heart disease or heart attack increases the odds by 30%.
- Higher General Health rating (inverse coded) is associated with a 79% decrease in diabetes risk.
- A cholesterol check was associated with a 268% increased odds of being diabetic—likely due to individuals with suspected conditions getting tested.
- Physical activity, smoking, and vegetable intake had no significant impact on diabetes risk.
- Variables such as mental health, education, and income had low or inverse effects on prediction.

### From Decision Tree Model:  
- Individuals with average general health (coded as 3) are more likely to be non-diabetic.
- Individuals with High Blood Pressure are more likely to be diabetic.
- People younger than 45 are generally non-diabetic.
- Obesity is strongly associated with diabetes diagnosis.
- Gender, physical activity, and alcohol consumption had no considerable predictive effect on diabetes in the tree model.

Note: The decision tree was pruned using cross-validated error metrics to reduce overfitting and maintain interpretability.  

## How to Run  
- Clone the repository and open the R script or RMarkdown file.
- Install required packages (rpart, ggplot2, caret, etc.)
- Load the cleaned dataset and run the models.
- Review outputs: confusion matrices, accuracy, and plots.
