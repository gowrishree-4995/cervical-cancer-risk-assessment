# cervical-cancer-risk-assessment

1. OVERVIEW
This project aims to assess the risk of cervical cancer based on various health and lifestyle factors. Using a machine learning model (XGBoost), the system takes user inputs through a simple front-end and predicts whether the individual is at high or low risk of developing cervical cancer. This project also highlights the importance of early detection and is developed as a proof-of-concept and educational tool, not a replacement for professional medical assessment.



2. PROJECT STRUCTURE
The project contains the following main files and folders:

train_and_save_model.py: Script to preprocess data, train the model, and save the trained model as xgb_model.pkl.
app.py: Flask application script to handle the frontend, get user inputs, and make predictions using the saved model.
templates/: Contains the HTML files for the frontend.
home.html: Provides general information and an introduction to cervical cancer.
index.html: Form for users to enter health-related data for risk assessment.
result.html: Displays the prediction result.
static/: Contains styles (styles.css) and images.



3.MODULAR BREAKDOWN

> Data Preprocessing:
Loaded the dataset and replaced missing values with the mean for continuous variables.
Dropped columns with minimal relevance or excessive missing values.
Converted data to a format suitable for model training.

> Model Training:
Used the XGBoost classifier due to its effectiveness in handling imbalanced data and complex relationships.
The model is trained with an 80/20 train-test split, with hyperparameters optimized for accuracy and interpretability.

> Prediction Flow:
User inputs health-related information via a web form.
Inputs are formatted and passed to the model to predict risk status.
Result (High/Low Risk) is displayed on the result.html page



4.MODEL SELECTION:

The XGBoost algorithm was selected for its strong performance in handling imbalanced data and ability to model non-linear relationships. 
The classifier was fine-tuned to improve precision and recall, critical metrics for health-risk prediction models.



5.FRONTEND:
The frontend is built using HTML/CSS with Flask as the backend framework. The home.html page introduces the project, and the index.html 
page collects user input for prediction.

