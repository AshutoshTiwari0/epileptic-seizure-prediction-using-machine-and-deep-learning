# Epileptic Seizure Detection using Machine Learning and Deep Learning

This project focuses on the detection of epileptic seizures using a dataset of EEG (electroencephalography) brain activity recordings. We utilize both machine learning and deep learning techniques to build a binary classifier distinguishing between seizure activity and non-seizure conditions.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation Metrics](#evaluation-metrics)
- [Installation](#installation)
- [Usage](#usage)

## Project Overview

In this project, we:

- Preprocessed the dataset containing 178 features for each subject, with the last column representing the seizure status (1 for seizure and 0 for non-seizure).
- Used **Principal Component Analysis (PCA)** to reduce dimensionality and make the model more efficient.
- Applied **RandomUnderSampler** to handle class imbalance.
- Trained a **Random Forest Classifier (RFC)** and **Artificial Neural Network (ANN)** model to detect epileptic seizures based on EEG signals.

## Dataset

The dataset used is a pre-processed version of the epileptic seizure detection data collected from the UCI Machine Learning Repository. The dataset contains recordings of brain activity (EEG) sampled over 23.5 seconds with 4097 data points for each subject.

- **Features**: 178 columns representing 178 data points for 1 second of EEG recording.
- **Target**: The target variable (`y`) is the label for each data point. The classes are:
  - **1**: Epileptic seizure
  - **0**: Non-seizure activity (includes classes 2, 3, 4, 5)

## Technologies Used

- **Python**: Programming language for data processing and model implementation.
- **Pandas & Numpy**: Data manipulation and analysis.
- **Scikit-learn**: Machine learning library used for Random Forest, PCA, StandardScaler, and model evaluation.
- **Keras (TensorFlow)**: Deep learning library for building and training the Artificial Neural Network (ANN).
- **Imbalanced-learn**: Used for handling class imbalance with **RandomUnderSampler**.
- **Matplotlib & Seaborn**: Visualization libraries.

## Data Preprocessing

1. **Data Loading**: The data is loaded from a CSV file (`Epileptic Seizure Recognition.csv`).
2. **Class Mapping**: Converted the multi-class problem to a binary classification problem by combining all non-seizure classes (2, 3, 4, 5) into class 0.
3. **Class Balancing**: Applied **RandomUnderSampler** to balance the dataset by reducing the majority class (non-seizures).
4. **Standardization**: Standardized the features using **StandardScaler** to ensure equal scale for the model.
5. **Dimensionality Reduction**: Used **Principal Component Analysis (PCA)** to reduce the feature space and retain 95% of the variance.

## Modeling

Two models were trained and evaluated for epileptic seizure detection:

1. **Random Forest Classifier (RFC)**:
   - A traditional machine learning model used for classification. 
   - Achieved **95.04% accuracy**, **95.89% precision**, and **94.04% recall**.

2. **Artificial Neural Network (ANN)**:
   - A deep learning model with two hidden layers and **ReLU** activation functions.
   - Trained using **binary cross-entropy loss** and **Adam optimizer**.
   - Achieved **95.04% accuracy**, **95.89% precision**, and **94.04% recall**.

## Evaluation Metrics

- **Accuracy**: Measures the percentage of correct predictions.
- **Precision**: The proportion of true positives in relation to all positive predictions.
- **Recall**: The proportion of true positives in relation to all actual positive instances.

## Installation

To run this project on your local machine, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/AshutoshTiwari0/epileptic-seizure-detection.git
   cd epileptic-seizure-detection

Install the required libraries: You can install the necessary dependencies using pip:

```bash
Copy code
pip install -r requirements.txt
```

Or, if you're using conda:

```bash
Copy code
conda install --file requirements.txt
```
Usage
Download the dataset Epileptic Seizure Recognition.csv and place it in the root directory of the project.

Run the Jupyter Notebook or the Python script to train the models and evaluate their performance:

```bash
Copy code
jupyter notebook
```
Or, if you prefer running it as a Python script:

```bash
Copy code
python epileptic_seizure_detection.py
```
Check the final results (Accuracy, Precision, Recall) and model evaluations in the output.

## Contributing
If you would like to contribute to this project, feel free to fork it, submit an issue, or create a pull request. Any improvements or suggestions are welcome!

