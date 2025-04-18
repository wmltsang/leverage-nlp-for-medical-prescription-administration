# Leverage-nlp-for-medical-prescription-administration

🧠 Disease Prediction Web App
This project leverages NLP and machine learning to predict diseases based on user-input symptoms. It includes a trained Logistic Regression model and a Streamlit interface that allows users to select symptoms and receive a disease prediction with a confidence score.

Developed in Python and hosted via Google Colab with LocalTunnel for web app exposure.

🔍 Key Features
Multi-symptom input via interactive UI

TF-IDF vectorization for text input

Pre-trained logistic regression model

Displays predicted disease and confidence score

Data preview from original dataset

🛠️ Files and Components
app.py
Main Streamlit app that:

Loads a trained model (disease_model.pkl) and vectorizer (tfidf_vectorizer.pkl) from Google Drive

Loads preprocessed symptom data (processed_diseases-2400_NER.csv)

Displays an interface to select symptoms and triggers prediction

Shows prediction result and confidence level

disease_model.pkl and tfidf_vectorizer.pkl
Pre-trained model and TF-IDF vectorizer saved via joblib.

processed_diseases-2400_NER.csv
CSV file containing disease and symptom mappings used to generate symptom options for prediction.

### Steps for users who want to run the files

 Firstly, please install the needed packages in the script, change the path after you clone down.  
 
 ### Enhancement:
 Deploy the app to Streamlit Community Cloud


####  High-Level Overview of the ML Pipeline
This project predicts likely diseases based on user-reported symptoms using a machine learning pipeline that combines natural language processing and logistic regression.

🔄 ETL Process
Data Source: A CSV file containing diseases, symptoms, and treatments.

Text Cleaning: Symptom text is standardized by lowercasing and splitting on various delimiters (e.g., commas, semicolons).

Feature Engineering: Symptoms are transformed into numerical features using TF-IDF vectorization.

🤖 Model
Algorithm: Logistic Regression

Target: Disease name (multi-class classification)

Training: Model is trained on the full dataset with class balancing to handle label imbalance.

Output: Given a set of symptoms, the model returns the top 5 most likely diseases along with confidence scores.

🚀 Deployment
The model and vectorizer are saved as .pkl files and loaded into a Streamlit web app.

Users can select symptoms via an interactive UI and receive immediate predictions.

The app is deployable on Streamlit Community Cloud or runnable via Google Colab using localtunnel.

