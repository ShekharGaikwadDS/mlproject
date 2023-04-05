## Machine Learning End-to-End Project

## The project consists of the following phases:

**Data Ingestion**
The data is first read as a CSV file. Then, the data is split into training and testing sets and saved as CSV files.

**Data Transformation**

In this phase, a ColumnTransformer Pipeline is created to transform the data. For numeric variables, SimpleImputer is applied with the strategy median, followed by standard scaling. For categorical variables, SimpleImputer is applied with the most frequent strategy, followed by ordinal encoding and standard scaling. This preprocessor is saved as a pickle file.

**Model Training**

In this phase, a base model is tested, and the best model found was the CatBoost Regressor. Hyperparameter tuning is performed on the CatBoost and KNN models. A final VotingRegressor is created, which combines the predictions of the CatBoost, XGBoost, and KNN models. This final model is saved as a pickle file.


**Prediction Pipeline**

This pipeline converts given data into a dataframe and has various functions to load the pickle files and predict the final results in Python.

**Flask App Creation**

A Flask app is created with a user interface to predict the gemstone prices inside a web application.

To use the application, simply run the Flask app and navigate to the URL in your web browser. You will be presented with a form to input the gemstone's attributes. Upon submission, the app will use the trained machine learning models to predict the gemstone's price.


**Requirements**

To run this project, you will need Python 3.7 or higher and the following Python packages:

Pandas
Scikit-learn
CatBoost
XGBoost
Flask
You can install these packages by running:

pip install -r requirements.txt


Usage

python app.py

This will start the Flask app, and you can navigate to the URL provided in the output to access the web application.





