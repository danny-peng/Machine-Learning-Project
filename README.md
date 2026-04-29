# Machine Learning Project: Bank Customer Churn Prediction

This project implements various machine learning models to predict customer churn for a bank using the BankChurners dataset.

## Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required packages: pandas, numpy, scikit-learn, matplotlib

## Setup

1. Clone or download the repository
2. Install required packages:
   ```bash
   pip install pandas numpy scikit-learn matplotlib jupyter
   ```

## Usage

### Data Preprocessing

Run the preprocessing notebook first to prepare the data:

1. Open `notebooks/01_preprocessing.ipynb`
2. Execute all cells to process the raw data and create train/validation/test splits
3. This will generate the processed CSV files in `data/processed/`

### Running Models

After preprocessing, you can run each model independently:

1. **Logistic Regression**: `notebooks/02_logistic_regression.ipynb`
   - Tests different feature transformations (no transformation, polynomial degree 2/3, logarithmic)
   - Evaluates various regularization parameters (lambda values)
   - Graphs performance metrics vs lambda values

2. **Support Vector Machine (SVM)**: `notebooks/03_SVM.ipynb`
   - Tests different kernel types (linear, RBF, polynomial degree 2/3)
   - Evaluates various regularization parameters (lambda values)
   - Graphs performance metrics vs lambda values

3. **Neural Network**: `notebooks/04_NN.ipynb`
   - Tests diferent neural network shapes (number of neurons, number of hidden layers)
   - Implements neural network models for churn prediction
   - Evaluates various regularization parameters (lambda values)
   - Graphs performance metrics vs lambda values

You can also analyze the dataset with the figures notebook:

1. **Figures**: `notebooks/figures.ipynb`
   - Contains visualizations and analysis of dataset

### Model Evaluation

Each model notebook evaluates performance using:
- Accuracy
- Precision
- Recall
- F1-Score

## Dataset

The project uses the BankChurners dataset from Kaggle, which contains customer information and churn labels for a bank. The dataset is pre-split into training, validation, and test sets during preprocessing.