Overview

This project is part of MGS 670 and focuses on solving a healthcare analytics problem using machine learning and deep learning techniques. The goal is to develop models that estimate the Hospital Length of Stay (HLOS) for patients based on various physiological and clinical features. The implementation is carried out using Python in Google Colab.

Objectives

Build predictive models to estimate HLOS:
Multi-Layer Perceptron (MLP) on pre-processed Data-at-admission.
Recurrent Neural Network (RNN) on pre-processed Days-breakdown data.
Preprocess datasets for effective feature engineering and train-test splitting.
Experiment with hyperparameters to optimize model performance.
Evaluate the models using the Mean Squared Error (MSE) metric.
Datasets

The following datasets are used for this project:

Data-at-admission: Includes patient characteristics, comorbidities, and vital signs recorded upon admission.
Days-breakdown: Provides daily physiological and clinical data for each patient up to 14 days post-admission.
Hospital-length-of-stay: Contains the actual HLOS values for each patient.
Medication-Static-List: Lists medications used in the hospital (used for context, not modeling).
Features

Independent Variables (Features):
Patient demographics: age, sex, height, weight.
Physiological metrics: systolic and diastolic blood pressure, heart rate, respiratory rate, oxygen saturation, temperature.
Laboratory results: WBC, RBC, hemoglobin, serum creatinine, sodium, potassium, etc.
Other metrics: intubated status, high-sensitivity cardiac troponin, CRP levels, etc.
Dependent Variable (Target):
Hospital Length of Stay (HLOS)
Project Steps

1. Data Preprocessing
Merge multiple datasets using the common patient ID.
Prepare a feature matrix including independent variables and target labels.
Handle missing data:
Identify columns with all missing values.
Compute and report statistics (e.g., mean, count).
Split the dataset into training (80%) and testing (20%) subsets.
2. Model Implementation
MLP for Data-at-admission:
Fit a multi-layer perceptron to predict HLOS.
Experiment with activation functions, optimizers, and hidden layers.
RNN for Days-breakdown:
Preprocess daily data into sequential format.
Use day-wise data and modified target values (e.g., remaining days).
Experiment with RNN architectures (e.g., LSTM, GRU).
3. Hyperparameter Tuning
Try different learning rates, batch sizes, number of epochs, and optimizers.
Evaluate models based on MSE and identify the best-performing configurations.
4. Evaluation
Report:
Number of rows and columns in the final dataset.
Mean values of each feature.
Columns with all zero values.
Model performance metrics (MSE).
Average and standard deviation of errors over multiple trials.
Key Results

Observations on dataset quality and preprocessing outcomes.
MSE scores for MLP and RNN models.
Discussion on model performance and potential improvements.
Challenges and Improvements

Challenges:
Handling large-scale sequential data for RNNs.
Computational limitations when working with extended daily data.
Improvements:
Incorporate feature selection to reduce dimensionality.
Explore advanced architectures like attention-based RNNs.
Submission Details


Technologies Used

Programming Language: Python
Tools: Google Colab, Pandas, NumPy, TensorFlow/Keras
Algorithms:
MLP: For tabular data from Data-at-admission.
RNN (LSTM/GRU): For sequential data from Days-breakdown.
