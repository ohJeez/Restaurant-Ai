Restaurant AI – Demand and Staff Forecasting System
Overview
Restaurant AI is a machine learning-based project developed to analyze restaurant operational data and generate predictions for food demand and staff requirements.

The system uses historical restaurant data to forecast the expected demand for food items and estimate the number of staff required during different time slots and operational roles. These predictions can support better planning and decision-making in restaurant operations.
Features
- Food demand prediction using historical sales data
- Preparation recommendations based on predicted demand
- Staff demand forecasting for different roles
- Time-slot-based staff planning
- Comparison of multiple machine learning models
- Model performance evaluation
- Feature importance analysis
- Actual versus predicted value visualization
Machine Learning Models
The following regression models were evaluated:
- Linear Regression
- Random Forest Regressor
- XGBoost Regressor
Food Demand Prediction Results
Model	MAE	RMSE	R² Score
Linear Regression	7.619416	9.951695	0.920985
Random Forest	7.502473	9.768210	0.923872
XGBoost	7.301468	9.557596	0.927119


Staff Demand Forecasting Results
Model	MAE	RMSE	R² Score
Linear Regression	3.045218	4.138918	0.901585
Random Forest	2.104383	2.732641	0.957100
XGBoost	2.070609	2.756420	0.956350


Dataset
The project uses restaurant-related datasets including:
- Sales data
- Menu item information
- Calendar information
- Staff information
- Staff schedules
- Historical validation data
Food Demand Features
Food demand prediction considers factors such as:
- Menu item
- Food category
- Date
- Day of the week
- Weekend and holiday information
- Promotions
- Weather conditions
- Previous sales values
- Lag features
- Rolling averages
Staff Demand Features
Staff forecasting considers:
- Orders handled
- Staff role
- Time slot
- Day of the week
- Date-related information
- Weekend information
Food Preparation Recommendation
The predicted food demand is used to generate preparation recommendations. The recommendation considers:
- Predicted demand
- Historical prediction error
- Preparation buffer
- Minimum batch requirements
This allows the system to provide a suggested preparation quantity for each food item.
Staff Planning
The staff forecasting model predicts the number of employees required for different:
- Roles
- Time slots
- Dates
The predicted values are converted into recommended staff requirements to support restaurant workforce planning.
Visualizations
The project includes visualizations such as:
- Actual versus predicted demand graphs
- Feature importance charts
- Model performance comparisons
- Food demand prediction analysis
- Staff requirement analysis
Project Structure
Restaurant-AI/
│
├── Demand_Model.ipynb
├── Staff_Demand_Model.ipynb
│
├── data/
│   ├── sales.csv
│   ├── menu_items.csv
│   ├── calendar.csv
│   ├── staff.csv
│   └── staff_schedule.csv
│
├── models/
│   ├── demand_model_v2.joblib
│   ├── demand_features.pkl
│   ├── staff_demand_model_final.joblib
│   └── staff_demand_features.pkl
│
└── README.md

Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Joblib
- Google Colab
Model Evaluation Metrics
The models were evaluated using:
- MAE (Mean Absolute Error) – Measures the average prediction error.
- RMSE (Root Mean Squared Error) – Measures the magnitude of prediction errors.
- R² Score – Measures how well the model explains variations in the data.
Conclusion
Restaurant AI demonstrates the application of machine learning techniques in restaurant operations. The project combines food demand prediction and staff demand forecasting to generate useful predictions and recommendations based on historical operational data.

The system provides a foundation for data-driven restaurant planning by using machine learning models to analyze demand patterns and workforce requirements.
Author
Jees Thomas Cleetus
MCA Student
Rajagiri College of Social Sciences
