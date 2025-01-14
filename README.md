# Crop Prediction Using Machine Learning

## Overview

Crop Prediction using Machine Learning is a project designed to assist farmers in making informed decisions about which crops to cultivate based on environmental and soil conditions. The project leverages two popular machine learning algorithms, **K-Nearest Neighbors (KNN)** and **Random Forest (RF)**, to predict the most suitable crop for a given set of input parameters. These parameters include soil nutrients (Nitrogen, Phosphorus, Potassium), climate conditions (temperature, humidity, rainfall), and soil pH levels.

The goal of this project is to provide farmers with a user-friendly tool that can help optimize crop yield by recommending the best crop to grow based on the specific conditions of their farmland.

---

## Features

- **Crop Prediction**: Predicts the optimal crop to cultivate based on input parameters such as soil nutrients, climate conditions, and soil pH.
- **Multiple Algorithms**: Utilizes both **K-Nearest Neighbors (KNN)** and **Random Forest (RF)** algorithms for crop prediction.
- **Web Interface**: Provides a simple and intuitive web interface for users to input data and view predictions.
- **Data Visualization**: Includes data visualization to explore the relationship between crop types and environmental factors.
- **Scalable and Modular**: The project is designed to be modular, allowing for easy integration of additional machine learning models or datasets.

---

## Algorithms Used

### 1. **K-Nearest Neighbors (KNN)**
   - KNN is a simple, non-parametric algorithm used for classification tasks. It predicts the class of a data point based on the majority class of its k nearest neighbors in the feature space.
   - **Advantages**: Easy to implement and interpret, no assumptions about the underlying data distribution.
   - **Use Case**: Used in this project to classify crops based on environmental and soil conditions.

### 2. **Random Forest (RF)**
   - Random Forest is an ensemble learning method that constructs multiple decision trees during training and outputs the mode of the classes (for classification) or the mean prediction (for regression) of the individual trees.
   - **Advantages**: Reduces overfitting, handles large datasets with higher dimensionality, and provides feature importance.
   - **Use Case**: Used in this project to improve prediction accuracy and robustness.

---

## Directory Structure

```
crop-prediction-using-ML/
├── README.md
├── KNN/
│   ├── Crop_recommendation.csv          # Dataset for crop prediction
│   ├── app.py                           # Flask application for KNN model
│   ├── crop_prediction_model.py         # Script to train and evaluate KNN model
│   ├── knn_model.pkl                    # Pre-trained KNN model
│   ├── main.py                          # Main script to run the KNN Flask app
│   ├── templates/                       # HTML templates for the web interface
│   │   ├── index.html                   # Home page for user input
│   │   ├── result.html                  # Page to display prediction results
│   │   └── style.css                    # CSS for styling the web pages
│   └── .idea/                           # PyCharm project configuration files
└── randomforest/
    ├── Crop_recommendation.csv          # Dataset for crop prediction
    ├── app.py                           # Flask application for Random Forest model
    ├── crop_prediction_model.py         # Script to train and evaluate Random Forest model
    ├── model.pkl                        # Pre-trained Random Forest model
    ├── main.py                          # Main script to run the Random Forest Flask app
    ├── tf.py                            # Additional script for model training and evaluation
    ├── templates/                       # HTML templates for the web interface
    │   ├── index.html                   # Home page for user input
    │   └── result.html                  # Page to display prediction results
    └── .idea/                           # PyCharm project configuration files
```

---

## Installation

### Prerequisites
- Python 3.x
- Flask
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn

### Steps to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/KoushikPraneeth/crop-prediction-using-ML.git
   cd crop-prediction-using-ML
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the KNN Model**:
   ```bash
   cd KNN
   python main.py
   ```
   - Access the web interface at `http://127.0.0.1:5000/`.

4. **Run the Random Forest Model**:
   ```bash
   cd randomforest
   python main.py
   ```
   - Access the web interface at `http://127.0.0.1:5000/`.

---

## Usage

1. **Input Parameters**:
   - On the home page, enter the following parameters:
     - Nitrogen (N), Phosphorus (P), Potassium (K) levels in the soil.
     - Temperature, Humidity, and Rainfall in your region.
     - Soil pH level.

2. **Get Prediction**:
   - Click on the "Predict Crop" button to get the recommended crop based on the input parameters.

3. **View Results**:
   - The predicted crop will be displayed on the results page.

---

## Dataset

The dataset used in this project is `Crop_recommendation.csv`, which contains the following features:

- **N**: Nitrogen content in the soil.
- **P**: Phosphorus content in the soil.
- **K**: Potassium content in the soil.
- **temperature**: Temperature in degrees Celsius.
- **humidity**: Relative humidity in percentage.
- **ph**: Soil pH level.
- **rainfall**: Rainfall in millimeters.
- **label**: The crop label (e.g., rice, maize, jute, etc.).

---

## Model Training and Evaluation

### KNN Model
- The KNN model is trained on the dataset and achieves an accuracy of **XX.XX%** on the test set.
- The model is saved as `knn_model.pkl` for use in the Flask application.

### Random Forest Model
- The Random Forest model is trained on the dataset and achieves an accuracy of **XX.XX%** on the test set.
- The model is saved as `model.pkl` for use in the Flask application.

---

## Future Improvements

- **Integration of More Algorithms**: Incorporate additional machine learning algorithms such as Support Vector Machines (SVM) or Gradient Boosting.
- **Real-Time Data Integration**: Integrate real-time weather and soil data for more accurate predictions.
- **Mobile Application**: Develop a mobile app for easier access and usability by farmers.
- **Multi-Language Support**: Add support for multiple languages to make the tool accessible to a wider audience.

---

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push your branch and submit a pull request.

---

## Acknowledgments

- Thanks to the creators of the dataset used in this project.
- Special thanks to the open-source community for providing valuable resources and tools.

---

Happy Farming! 🌱
