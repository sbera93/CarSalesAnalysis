# CarSalesAnalysis

Data https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data

---

### **Car Sales Prediction Report**

#### **1. Data Overview**
The dataset contains information on over half a million car sales, including details such as:
- **Make**, **Model**, and **Trim** of the car.
- **Odometer reading** (miles driven).
- **Market value** (MMR).
- **Selling price** of the car.
- **Condition**, **Transmission**, **Body type**, and other related attributes.

The goal of this analysis is to predict the **selling price** of the cars based on these various features using machine learning techniques.

#### **2. Data Cleaning and Preprocessing**
The initial data cleaning process focused on handling missing values and ensuring that the dataset was ready for analysis:

- **Missing Data Handling**:
  - Critical columns (`sellingprice`, `condition`, `odometer`) with missing values were dropped.
  - Non-critical columns such as `make`, `model`, `trim`, `body`, `transmission`, and others were filled with appropriate default values (`'Unknown'`), except for the `mmr` column, which was imputed using the median value.

- **Outliers and Invalid Entries**:
  - The dataset was checked for any extreme outliers, and invalid entries (such as incorrect date formats) were removed. The dataset was cleaned and verified to have no missing values after these steps.

#### **3. Exploratory Data Analysis (EDA)**
Once the data was cleaned, an initial exploration was performed:

- **Descriptive Statistics**:
  - Key variables such as **odometer** (miles driven), **sellingprice**, and **condition** were explored to understand their distributions and detect any unusual patterns.
  
- **Feature Analysis**:
  - **Condition** had a range from 0 to 100, indicating the car's condition.
  - **Odometer** represented the total miles driven by the car, which is an important predictor for the price.
  - **Market value (MMR)** showed some correlation with the **sellingprice** but was not always an exact match, implying that market conditions or other factors affect the final sale price.

#### **4. Predictive Modeling**
A machine learning model was built to predict the **selling price** based on the other features in the dataset.

- **Model Choice**:
  - A **Random Forest Regressor** was chosen for the task due to its ability to handle a variety of data types and its robustness against overfitting.

- **Evaluation Metrics**:
  - **R-squared (R²)**: This metric showed how well the model explained the variance in the selling prices. The R² score from the model indicated that a significant portion of the variance in the selling price could be attributed to the features used.
  
  - **Root Mean Squared Error (RMSE)**: The RMSE indicated the average error between predicted and actual selling prices. This metric helps assess the model’s accuracy in practical terms.

#### **5. Model Performance and Feature Importance**
- The model successfully predicted the **selling price** with reasonable accuracy, but further optimizations and tuning are necessary to improve performance, especially in the case of expensive vehicles.
  
- **Feature Importance**:
  - Some features, such as **odometer**, **condition**, and **MMR**, were found to be highly influential in predicting the selling price of cars. These insights can guide future feature engineering or data collection efforts.

#### **6. Performance Breakdown by Price Range**
To better understand the model’s performance across different price segments, an analysis of RMSE and R² was conducted across several price ranges (e.g., $0 - $20,000, $20,000 - $40,000, etc.).

- The model's performance was found to decrease as the price increased, which is expected due to the larger variation in prices for high-value cars.

#### **7. Conclusion and Next Steps**
Based on the findings from this analysis, the following conclusions can be made:

- **Model Effectiveness**: The model provides a good baseline for predicting car prices, but improvements are needed for high-priced vehicles. Techniques like **hyperparameter tuning** or experimenting with other models (e.g., **Gradient Boosting** or **XGBoost**) could improve predictions.
  
- **Feature Engineering**: Additional features such as **make**, **model**, or location-specific variables could be incorporated to improve the model's performance.

- **Next Steps**:
  1. Explore more sophisticated algorithms to improve model accuracy.
  2. Conduct further experiments to handle high-priced vehicles more effectively.
  3. Incorporate additional data sources (e.g., car make, location, or seasonal factors).

This concludes the analysis, and further improvements can be explored to enhance the prediction of car prices.

---

Let me know if you would like to explore any part of the analysis further or refine any sections of the report!
