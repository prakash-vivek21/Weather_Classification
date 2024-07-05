# Weather_Classification

### Table of Content
* Introduction
* Dataset
* Preprocessing
* Visualization
* Classification Techniques and Insights
* Conclusion

### Introduction
Weather classification is a critical task in meteorology, impacting various sectors including agriculture, transportation, and disaster management. Accurate weather predictions help in making informed decisions and preparing for adverse conditions. This project aims to predict the type of weather using a variety of machine learning models based on historical weather data.
The dataset contains several features that describe different aspects of the weather, both numerical (e.g., temperature, humidity) and categorical (e.g., season, location). By leveraging these features, the project builds and evaluates multiple classification models to identify the most accurate and robust predictors of weather type.

### Dataset
* Temperature: The ambient temperature measured in degrees Celsius.
* Humidity: The percentage of humidity in the air.
* Wind Speed: The speed of the wind measured in kilometers per hour (km/h).
* Precipitation (%): The probability of precipitation expressed as a percentage.
* Cloud Cover: the cloud cover is categorical and has values like partly cloudy, clear, overcast, cloudy.
* Atmospheric Pressure: The pressure exerted by the atmosphere at a given point, measured in hectopascals (hPa).
* UV Index: The level of ultraviolet radiation exposure.
* Visibility (km): The distance one can see as determined by light and weather conditions, measured in kilometers.
* Season: The time of the year, categorized into distinct seasons (Winter, Spring, Summer, Autumn).
* Location: The geographic location where the weather data was collected like inland, mountain or coastal.
* Weather Type: The classification label for the type of weather, which is the target variable for prediction and has values like Rainy, Cloudy, Sunny or Snow.

### Data Preprocessing
* Handle missing values: there were no missing values.
* Handling outliers: Outliers were found in the features and hence the features were scaled using Robust Scaler for effective oulier handling.
* Feature Engineering: label encoding of the categorical features using LabelEncoder.
* Splitting Data: Dividing the dataset into training and testing sets.

### Data Visualization
* Box Plot: Used to analyze the presence and distribution of outliers in the dataset.
* Pair Plot: Utilized to examine the relationships between continuous features.
* Pie Chart: Employed to visualize the distribution of categorical features within the dataset.
* Scatter Plot: Applied to study the relationships between features and their impact on the target variable.

### Classification Techniques
* Random Forest Classifier: Random Forest achieves the highest cross-validation score among all models, indicating robust performance in classifying multiple classes based on the provided features.The ensemble nature of Random Forest, combining multiple decision trees, proves effective for handling complex interactions and achieving high predictive accuracy.
    
* Support Vector Machine: SVC achieved the second-highest cross-validation score (91.19%), indicating strong performance but slightly lower than Random Forest. The choice of C=10 suggests a relatively high regularization parameter, with the RBF kernel and automatic gamma setting adapting well to the data.
 
* K-Nearest Neighbors: Shows a competitive score (90.23%) but slightly lower compared to Random Forest and SVC. Performance influenced by choice of k (number of neighbors) and distance metric used.
  
* Logistic Regression: Shows the lowest cross-validation score (83.34%) among all models evaluated. Assumes a linear relationship between input features and output, which may not capture complex interactions in the data as effectively.

* Gradient Boosting:Achieves a competitive score (90.61%) close to the top performers. Improves model performance iteratively by focusing on correcting errors made by previous models in the ensemble. Utilizes decision trees as base learners, emphasizing the strengths of sequential model building.

* XGBoost Classifier: Performs similarly well to Random Forest and SVC (91.24%). Leverages gradient boosting to improve model performance iteratively. Capable of handling complex interactions and boosting model performance through feature importance analysis.

##### Hyperparameter Tuning: Hyperparameter tuning was performed using GridSearchCV to find the best parameters for Random Forest and SVC.

### Conclusion
Each model offers distinct advantages based on their performance and parameter settings. Random Forest, SVC, and XGBoost emerge as top performers, demonstrating strong cross-validation scores above 91%. Logistic Regression, while simpler and interpretable, shows limitations in capturing complex data patterns compared to ensemble methods like Random Forest and XGBoost. KNN and Gradient Boosting also perform well but slightly below the top models, emphasizing the importance of model selection based on specific task requirements and dataset characteristics.

