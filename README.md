#   Quality Prediction in Mining Process

# About Dataset
# Context
It is not always easy to find databases from real world manufacturing plants, specially mining plants. So, I would like to share this database with the community, which comes from one of the most important parts of a mining process: a flotation plant!.

The main goal is to use this data to predict how much impurity is in the ore concentrate. As this impurity is measured every hour, if we can predict how much silica (impurity) is in the ore concentrate, we can help the engineers, giving them early information to take actions (empowering!). Hence, they will be able to take corrective actions in advance (reduce impurity, if it is the case) and also help the environment (reducing the amount of ore that goes to tailings as you reduce silica in the ore concentrate).

# Content
The first column shows time and date range (from march of 2017 until september of 2017). Some columns were sampled every 20 second. Others were sampled on a hourly base.The second and third columns are quality measures of the iron ore pulp right before it is fed into the flotation plant. Column 4 until column 8 are the most important variables that impact in the ore quality in the end of the process. From column 9 until column 22, we can see process data (level and air flow inside the flotation columns, which also impact in ore quality. The last two columns are the final iron ore pulp quality measurement from the lab.Target is to predict the last column, which is the % of silica in the iron ore concentrate.

# Existing  solution
Existing solutions for quality prediction in mining processes often involve the application of machine learning and statistical modeling techniques. Some common methods used include:

Regression Models: Linear regression and its variants are commonly employed to predict the quality of the mining process based on input features such as temperature, ore composition, and other process parameters.

Classification Models: Classification algorithms, such as decision trees, random forests, and support vector machines, can be used to classify the quality of the mining process into discrete categories (e.g., high, medium, low) based on input features.

Time Series Analysis: If the dataset contains temporal information, time series analysis techniques like ARIMA or LSTM (Long Short-Term Memory) networks can be used to capture temporal dependencies and predict the quality of future mining processes. 

# Limitations
•	Limitations of existing solutions can vary depending on the specific methods employed and the characteristics of the dataset. Some common limitations include:
•	Limited Feature Set: If the dataset lacks important features or if relevant information is missing, it can impact the accuracy and reliability of the predictions.
•	Data Quality: Poor data quality, such as missing values, outliers, or inconsistencies, can affect the performance of prediction models.
•	Lack of Domain Knowledge: Without a deep understanding of the mining process, it can be challenging to select appropriate features, interpret the results, or address specific domain-related challenges.
•	Scalability: Some models may not scale well to large datasets or real-time prediction requirements, which can limit their practical application in mining operations.

# Proposed solution
The proposed solution for the "Quality Prediction in a Mining Process" involves several steps. First, we process dataset needs to be explored and preprocessed, addressing any missing values, outliers, or data quality issues. Feature engineering techniques can be applied to create new features based on domain knowledge and the mining process. Next, suitable machine learning models are selected, such as regression or classification algorithms, and trained on the dataset. Next, hyperparameter tuning was performed using GridsearchCV and lastly the models were finalized and validated with the best estimator previously discovered during the tuning phase. The results of the models are interpreted and analyzed to gain insights into the factors influencing the quality prediction.

# Performance Outcome
After using various algorithm’s, we documented their performance using the RMSE score, R^2, and accuracy. We found out that the Gradient Boosting Regressor performed better on the resampled dataset that aggregated the values every hour from the original dataset. We were able to predict the % Silica Concentrate with an accuracy of 93.80% on the large original dataset and an accuracy of 62.89% on the small resampled dataset.


# Reference
[1]  https://www.researchgate.net/publication/237086918_A_Data_Mining_Approach_for_De veloping_Quality_Prediction_Model_in_Multi-Stage_Manufacturing.	
[2]  https://www.sciencedirect.com/science/article/pii/S1474034620300707.
[3]  https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process
[4]  https://link.springer.com/article/10.1007/s10845-022-01963-8 Machine learning and deep learning predictive quality in manufacturing.




