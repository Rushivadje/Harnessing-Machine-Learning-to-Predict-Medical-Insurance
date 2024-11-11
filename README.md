# Harnessing-Machine-Learning-to-Predict-Medical-Insurance-Pricing-Trends

# Overview
This project aims to predict medical insurance costs based on various demographic, health, and lifestyle factors using machine learning. After exploring and testing several models, the XGBoost Regressor was selected as the final model for deployment due to its superior accuracy and robustness. The model was saved using pickle and deployed via Streamlit to create an easy-to-use, web-based interface.

# Project Structure
1. Problem Definition

   The goal is to develop a predictive model that estimates individual medical insurance charges based on user characteristics. This enables insurance providers to 
   set fair premiums based on risk and offers insights into factors contributing to insurance costs.

2. Data Collection

   The dataset for this project consists of 1,338 records with information on individuals’ demographics, health metrics, and insurance charges. Each entry includes 
   the following features:

        Age:       Age of the primary beneficiary
    
        Sex:       Gender (male or female)
    
        BMI:       Body Mass Index, a measure of body fat based on height and weight
    
        Children:  Number of children covered by insurance
    
        Smoker:    Smoking status (yes or no)
    
        Region:    Residential area of the beneficiary in the US
    
        Charges:   The medical insurance cost to be predicted (target variable)

4. Data Cleaning and Preprocessing

   The following steps were taken to ensure the data was clean and prepared for modeling:

        Handling Missing Values: Verified that there were no missing entries.
    
        Encoding Categorical Variables: Used label encoding to convert categorical variables (e.g., sex, smoker status, region) into numerical form.
    
        Feature Scaling: Standard scaling was applied to continuous variables, such as age and BMI, for optimized model performance.

4. Exploratory Data Analysis (EDA)

   EDA was conducted to uncover relationships between features and the target variable:

        Age and Charges: Older individuals typically incur higher charges.

        BMI and Charges: Higher BMI correlates with increased charges, especially for smokers.
    
        Smoking Status: Smokers have significantly higher insurance charges, showing the health risk associated with smoking.

   Key Visualizations:

    Correlation heatmap and distribution plots of charges by smoking status, BMI, and age are available in the project files to illustrate these relationships.

6. Feature Engineering and Selection

        Feature Engineering: Created derived features or adjusted existing features to capture patterns better.
        
        Feature Selection: The features that had the highest predictive power for insurance charges (e.g., age, BMI, smoking status) were selected based on 
        correlation analysis and feature importance in preliminary models.

8. Model Selection

   The following models were considered and tested for this project:

        Linear Regression
    
        Random Forest Regressor

        Gradient Boosting Regressor
    
        XGBoost Regressor

    A Model Performance Comparison Table:
    
        Model	              MAE (Mean Absolute Error)  	R-squared

        Linear Regression       	3673	                  0.8133

        Random Forest       	        2354	                  0.8817

        Gradient Boosting       	2075	                  0.9176

        XGBoost (Final)       	        2052 (best)	          0.9203 (best)
    
    Based on this comparison, the XGBoost Regressor was chosen as the final model for its accuracy and ability to capture complex patterns in the data.

7. Model Training

   The XGBoost Regressor was trained on the preprocessed dataset, with hyperparameters tuned to improve its performance. Fine-tuning of parameters, such as 
   learning rate and max depth, resulted in optimal accuracy.

8. Model Evaluation and Tuning

   The final model was evaluated using Mean Absolute Error (MAE) and R-squared metrics to gauge prediction accuracy and explainability. Cross-validation was also      employed to ensure the model’s robustness.

10. Model Deployment

    The trained XGBoost model was saved using pickle for reusability and deployed via Streamlit to provide an accessible interface for users. Through this             interface, users can enter demographic and health data to receive an instant prediction of their insurance charges.

# Example Prediction

Users can test the model by entering sample values. For instance:

    Input:
      
      Age: 19
      BMI: 27.9
      Children: 0
      Smoker: Yes

    Predicted Charge: $18,006 (example output)

This helps users understand the model’s predictions in a practical context.

# Results
The XGBoost model outperformed other models, achieving the lowest MAE and highest R-squared values. The web-based interface provides reliable predictions based on the provided features.

# Future Work
To further enhance this project:

    Add More Features: Additional features, such as lifestyle habits, medical history, and physical activity level, could improve model accuracy.
    
    Further Tuning: Additional tuning of XGBoost hyperparameters could yield marginal gains in predictive power.
   
    Optimize Deployment: Using more advanced deployment methods like cloud hosting could scale the model for broader use.

# Ethical Considerations
This model uses demographic and health data to predict insurance costs. Although educational, the model highlights sensitive issues, such as premium bias based on age or smoking status. Real-world implementations should take these ethical considerations into account and use data responsibly.

# Glossary of Terms

      BMI (Body Mass Index): A measure of body fat calculated as weight (kg) / height^2 (m).
      
      XGBoost: A gradient boosting library optimized for predictive accuracy and speed, widely used in machine learning competitions.
      
      Mean Absolute Error (MAE): A measure of prediction error, where lower values indicate better accuracy.
      
      R-squared: A statistical measure indicating how well data points fit a regression line, with values closer to 1 showing a better fit.

# Contributing
Contributions are welcome! Please submit a pull request or open an issue if you have suggestions or improvements.
