# Predictive-Maintenance-for-Industrial-Equipment
# Objective:
This project focuses on developing machine learning models to predict equipment failures in an industrial manufacturing environment. By analyzing sensor data, the aim is to implement predictive maintenance, minimizing downtime, reducing maintenance costs, and improving operational efficiency by identifying potential equipment failures before they occur.

# Project Structure:
Data: The dataset used contains sensor readings such as air temperature, process temperature, rotational speed, torque, tool wear, and failure types. It includes both normal and anomalous operational conditions.

Models:

Classification Models: Used to predict equipment failure and the type of failure.
Regression Models: Used to predict tool wear and identify patterns in machine operation.
Anomaly Detection: Identifies abnormal operational conditions that could indicate potential failures.
## Results:
# 1. Failure Prediction (Classification):
The classification model to predict machine failures produced the following results:

Confusion Matrix:

True Negatives (0 predicted as 0): 1939
False Positives (1 predicted as 0): 0
False Negatives (0 predicted as 1): 2
True Positives (1 predicted as 1): 59
Performance Metrics:

Precision: 100% for class 1 (machine failure).
Recall: 97% for class 1 (machine failure).
F1-Score: High for both classes, indicating a balanced performance.
Accuracy: 99.9%, showing exceptional model performance.
Next Steps:

Check for overfitting by comparing training vs test data performance.
Use balancing techniques like oversampling or undersampling if the dataset is imbalanced.
Hyperparameter tuning for further improvement.
Explore additional feature engineering.
# 2. Failure Type Prediction:
The model was trained to predict specific types of machine failures, such as heat dissipation, power failure, overstrain, etc.

Confusion Matrix: The matrix indicates correct and incorrect predictions for each failure type.

Performance Metrics:

Heat Dissipation Failure: Precision 1.00, Recall 0.95
No Failure: No correct predictions, resulting in poor performance.
Overstrain Failure: Precision 0.89, Recall 1.00
Power Failure: Precision 0.65, Recall 0.92
Tool Wear Failure: Precision 1.00, Recall 0.80
Overall Accuracy: 88.24%
Next Steps:

Address class imbalance using resampling techniques like SMOTE.
Experiment with model tuning and feature engineering.
# 3. Tool Wear Prediction (Regression):
The model's performance in predicting tool wear produced the following results:

Mean Squared Error (MSE): 4048.75 (high, indicating poor prediction accuracy).

R-squared Score: 0.052 (low, indicating the model explains only 5.2% of the variance).

Next Steps:

Explore additional features and refine existing features.
Handle outliers and perform data preprocessing to improve performance.
Tune hyperparameters and try different regression models like Gradient Boosting or Support Vector Regression (SVR).
# 4. Anomaly Detection:
Anomalies in the operational data were detected using the Isolation Forest model. These anomalies represent deviations from normal conditions, potentially indicating issues leading to machine failure.

Detected Anomalies: Examples include deviations in air temperature, process temperature, rotational speed, torque, and tool wear, often associated with power failure events.

Next Steps:

Continue exploring operational patterns that result in anomalies and failure.
Investigate the root causes of anomalies to improve operational efficiency.
How to Run:
# Clone the repository:
bash
Copy code
git clone https://github.com/puckuz/predictive-maintenance-for-Industrial-Equipment.git
Navigate to the project directory:
bash
Copy code
cd predictive-maintenance
Install the necessary packages:
Copy code
pip install -r requirements.txt
Run the analysis:
css
Copy code
python main.py
## Future Work:
Apply techniques like cross-validation, regularization, and simpler models to address potential overfitting.
Perform hyperparameter tuning to enhance model performance.
Use techniques like SMOTE to address class imbalance.
Explore additional sensor data for feature engineering.
## Contributions:
Feel free to contribute by opening a pull request or suggesting improvements.

## License:
This project is licensed under the MIT License.
