# Customer Churn Prediction

## Overview

This project predicts whether telecom customers are likely to leave their service using machine learning. It uses customer information such as tenure, monthly charges, total charges, and subscribed services to identify potential churn.

Two machine learning models, Random Forest and XGBoost, are implemented and evaluated. The project also uses hyperparameter tuning and feature importance analysis to improve model performance and identify the factors influencing customer churn.

## Dataset

- **File:** `customer_churn_data.csv`
- **Target Variable:** `Churn` (Yes/No)
- **Features:** Customer demographics, tenure, monthly charges, total charges, and service-related information.

**Note:** The dataset is not included in the repository. You must place `customer_churn_data.csv` in the project directory before running the script.

## Project Structure

```text
customer-churn-prediction/
│
├── churn_prediction.py   # Data preprocessing, model training, and evaluation
├── requirements.txt      # Required Python libraries
├── README.md             # Project documentation
└── .gitignore             # Files excluded from Git
```

**Note:** The dataset (`customer_churn_data.csv`) and saved model files (`churn_model.pkl` and `label_encoder.pkl`) are not included in the repository. The model files are generated when the script is executed, provided the implementation saves them successfully.

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/snehapuniya15-ship-it/customer-churn-prediction.git
cd customer-churn-prediction
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment.

**Mac/Linux:**
```bash
source venv/bin/activate
```

**Windows:**
```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the Dataset

Place `customer_churn_data.csv` in the project directory.

## Usage

Run the main Python script:

```bash
python churn_prediction.py
```

The script performs the following operations:

1. Loads the customer churn dataset.
2. Preprocesses the data for machine learning.
3. Trains the Random Forest and XGBoost models.
4. Tunes XGBoost hyperparameters using GridSearchCV.
5. Evaluates model performance using accuracy, precision, recall, and F1-score.
6. Identifies important features influencing customer churn.
7. Saves the trained model and label encoder, as implemented in the script.

## Models and Evaluation

### Random Forest
- Uses an ensemble of decision trees to predict customer churn.
- Employs balanced class weights to help address class imbalance.
- Uses a maximum tree depth of 5.

### XGBoost
- Uses gradient boosting to identify patterns associated with customer churn.
- Applies GridSearchCV for hyperparameter optimization.

### Evaluation Metrics

The models are evaluated using the following metrics:

- **Accuracy:** Measures the proportion of correct predictions.
- **Precision:** Measures how many predicted churn cases are actually churn cases.
- **Recall:** Measures how many actual churn cases are correctly identified.
- **F1-score:** Balances precision and recall.

### Feature Importance

Feature importance analysis helps identify which customer characteristics contribute most to churn predictions. These insights can help businesses understand customer behavior and develop retention strategies.

## Dependencies

The project uses Python libraries listed in `requirements.txt`, including:

- pandas
- NumPy
- scikit-learn
- XGBoost
- joblib

## Future Improvements

- Add visualizations for feature importance and model performance.
- Experiment with additional machine learning models, such as Neural Networks and LightGBM.
- Develop a web application using Flask to make churn predictions through a user-friendly interface.

## Author

**Sneha Puniya**

- **Email:** snehapuniya15@gmail.com
- **GitHub:** [snehapuniya15-ship-it](https://github.com/snehapuniya15-ship-it)
- **Project Repository:** [Customer Churn Prediction](https://github.com/snehapuniya15-ship-it/customer-churn-prediction)

## License

This project is licensed under the MIT License.