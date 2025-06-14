# Online Payments Fraud Detection with Machine Learning

[![Python](https://img.shields.io/badge/python-v3.7+-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/flask-v2.0+-green.svg)](https://flask.palletsprojects.com/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-latest-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview

This project implements a machine learning-based system for detecting fraudulent online transactions. Using historical transaction data and advanced machine learning techniques, the system provides real-time fraud detection through a user-friendly web interface.

## Features

- Real-time fraud detection for online transactions
- Web-based user interface built with Flask
- Machine learning model trained on transaction data
- Interactive data visualization
- REST API for integration

## Dataset Description

The model is trained on the [PaySim synthetic dataset](https://www.kaggle.com/ealaxi/paysim1/download) from Kaggle, which contains the following features:

* `step` : represents a unit of time where 1 step equals 1 hour
* `type` : type of online transaction
* `amount` : the amount of the transaction
* `nameOrig` : customer starting the transaction
* `oldbalanceOrg` : balance before the transaction
* `newbalanceOrig` : balance after the transaction
* `nameDest` : recipient of the transaction
* `oldbalanceDest` : initial balance of recipient before the transaction
* `newbalanceDest` : the new balance of recipient after the transaction
* `isFraud` : fraud transaction (target variable)

## Technical Implementation

### Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn
- Flask
- matplotlib
- seaborn
- plotly

### Model Details

The fraud detection system uses a Decision Tree Classifier trained on the following features:
- Transaction type
- Transaction amount
- Original balance
- New balance

The model achieves good accuracy in detecting fraudulent transactions and is deployed via a Flask web application.

## Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/[your-username]/Online_fraud_detection.git
cd Online_fraud_detection
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Unix or MacOS:
source venv/bin/activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage

1. Start the Flask application:
```bash
python app.py
```

2. Open your web browser and navigate to `http://localhost:5000`
3. Enter the transaction details in the form
4. Submit to get the fraud detection result

## Project Structure

```
├── app.py              # Flask web application
├── main.ipynb          # Jupyter notebook with model development
├── static/
│   ├── model.pkl       # Trained model
│   └── style.css       # Web interface styling
└── templates/
    └── index.html      # Web interface template
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.

## Acknowledgments

- The code in this project was inspired by the [article on Online Payments Fraud Detection](https://thecleverprogrammer.com/author/amankharwal/)
- Dataset provided by PaySim synthetic financial dataset
