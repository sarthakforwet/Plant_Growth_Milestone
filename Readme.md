Plant Growth Feature Engineering and Binary Classification Pipeline
This repository contains a TensorFlow-based pipeline for feature engineering and binary classification on a plant growth dataset. The pipeline includes data preprocessing, feature engineering, model training, and evaluation. The target variable is Growth_Milestone.

Table of Contents
Introduction
Dataset
Pipeline Steps
Model Training
Evaluation
Results
Usage
Dependencies
License
Introduction
This project demonstrates how to create a feature engineering pipeline using TensorFlow and train a binary classification model to predict plant growth milestones. The pipeline handles both numerical and categorical features, applies scaling and encoding, and trains a neural network model.

Dataset
The dataset used for this project includes the following columns:

Sunlight_Hours (numerical)
Temperature (numerical)
Humidity (numerical)
Soil_Type (categorical)
Fertilizer_Type (categorical)
Growth_Milestone (binary label)
Pipeline Steps
Convert DataFrame to Dataset: The training dataset is converted from a DataFrame into a TensorFlow Dataset object, shuffled, and batched.
Numerical Columns: Sunlight_Hours, Temperature, and Humidity are converted to numeric columns and scaled using MinMax scaling.
Categorical Columns: Soil_Type and Fertilizer_Type are formatted and one-hot encoded.
Bucketizing: Temperature and Humidity are bucketized into specified ranges.
Feature Columns: All feature columns are tracked in a list.
Feature Cross: A feature cross is applied among Soil_Type and Fertilizer_Type.
Model Training
The model is a neural network with the following layers:

A DenseFeatures layer for the feature columns
Two hidden Dense layers with ReLU activation
An output Dense layer with sigmoid activation
The model is compiled with the Adam optimizer, binary cross-entropy loss, and accuracy metric. It is trained for 10 epochs.

Evaluation
The model is evaluated on a test set using accuracy as the metric. Training and validation accuracy and loss are visualized.

Results
The training and validation accuracy and loss over the epochs are plotted to visualize the model's performance.

Usage
To use this pipeline, follow these steps:

Clone the repository:

sh
Copy code
git clone https://github.com/yourusername/plant-growth-classification.git
cd plant-growth-classification
Install dependencies:

sh
Copy code
pip install -r requirements.txt
Run the pipeline:

sh
Copy code
python feature_engineering_pipeline.py
View the results:
After running the script, training and validation accuracy and loss plots will be generated.

Dependencies
Python 3.6+
TensorFlow 2.x
Pandas
NumPy
Matplotlib
Install the dependencies using:

sh
Copy code
pip install tensorflow pandas numpy matplotlib
License
This project is licensed under the MIT License. See the LICENSE file for details.
