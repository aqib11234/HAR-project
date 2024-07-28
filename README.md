# HAR-project
This project focuses on Human Activity Recognition (HAR) using the UCI HAR dataset. The goal is to classify activities such as walking, sitting, and standing based on accelerometer and gyroscope data from smartphones. The project utilizes machine learning techniques, including data preprocessing, feature extraction, and neural network modeling, to achieve accurate classification.

Project Overview
Objective: To develop a machine learning model that accurately classifies six different human activities using sensor data.
Dataset: UCI HAR Dataset, containing 561 features derived from accelerometer and gyroscope signals.
Techniques Used:
Data preprocessing (normalization, imputation)
Dimensionality reduction (PCA)
Neural network modeling with Keras
Hyperparameter tuning using KerasTuner
Data Preprocessing
Imputation: Missing values were handled using the mean imputation method.
Normalization: Features were normalized using MinMaxScaler to ensure they are on the same scale.
Dimensionality Reduction: Principal Component Analysis (PCA) was applied to reduce the feature set from 561 to 100 components, capturing most of the variance in the data.
Feature Extraction
Two types of features were extracted:

Time Domain Features: Mean, standard deviation, skewness, and kurtosis.
Frequency Domain Features: FFT-based features like mean, standard deviation, skewness, and kurtosis of the transformed data.
Model Development
A neural network was developed using Keras with the following structure:

Multiple dense layers with varying units and dropout rates.
ReLU activation function for hidden layers and softmax for the output layer.
The model was trained on PCA-transformed data and evaluated for accuracy.
Hyperparameter Tuning
KerasTuner was used to explore different configurations of the neural network, optimizing for validation accuracy. This process involved tuning:

The number of layers and units per layer
Dropout rates
Activation functions
Results
The final model achieved high accuracy on the test set, demonstrating its effectiveness in classifying human activities based on sensor data.

Challenges and Solutions
High Dimensionality: Addressed using PCA and normalization.
Model Overfitting: Mitigated with dropout regularization and cross-validation.
Achieving High Accuracy: Achieved through extensive hyperparameter tuning and advanced model architectures.
Conclusion
This project successfully demonstrates the application of machine learning techniques for human activity recognition. Future work could explore more advanced deep learning models, such as LSTMs or CNNs, and incorporate additional data sources for improved accuracy.

How to Use
Clone the repository.
Install the required dependencies listed in requirements.txt.
Run the Jupyter notebooks to explore data preprocessing, feature extraction, and model training.
