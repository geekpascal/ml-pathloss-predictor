---
title: Pathloss Predictor
emoji: 📡
colorFrom: indigo
colorTo: gray
sdk: docker
license: mit
short_description: A web app that utilizes ANN, CNN, and DNN models to accurately predict signal path loss.
---

<div align="center">
  <h1 align="center">Pathloss Predictor 🛰️</h1>
  <p align="center">
    A web application for predicting signal path loss using various machine learning models.
    <br />
    <a href="https://pascalx-pathloss-predictor.hf.space" target="_blank"><strong>View Live Demo »</strong></a>
    <br />
    <br />
    <a href="https://github.com/geekpascal/ml-pathloss-predictor/issues">Report Bug</a>
    ·
    <a href="https://github.com/geekpascal/ml-pathloss-predictor/issues">Request Feature</a>
  </p>
</div>

---

## About The Project


> **Note**: You should replace the line above with a screenshot of your application's web interface!

This project is a user-friendly web application designed to predict signal path loss using three different pre-trained machine learning models: **Artificial Neural Networks (ANN)**, **Convolutional Neural Networks (CNN)**, and **Deep Neural Networks (DNN)**.

The application provides a simple web UI and a REST API to make complex path loss calculations accessible for various use cases.

---

## ✨ Features

- **Multiple Model Support**: Predict path loss using your choice of pre-trained ANN, CNN, or DNN models.
- **Intuitive Web Interface**: A clean and simple UI for inputting parameters and viewing results.
- **REST API Endpoint**: Programmatically access the prediction models via a simple `/api/predict` endpoint.
- **Health Check**: A `/health` endpoint to monitor the status of the application and loaded models.
- **Dockerized for Portability**: Easily deploy and run the application in a containerized environment.

---

## 🛠️ Built With

This project was built using the following technologies:

* **Flask**: For the web framework and backend logic.
* **TensorFlow/Keras**: For loading and using the pre-trained models.
* **Scikit-learn**: For data pre-processing.
* **Docker**: For containerization and deployment.
* **HTML/CSS**: For the front-end structure and styling.

---

## 🚀 Getting Started

You can run this project locally for development or testing.

### Prerequisites

* Python 3.8+
* pip (Python package installer)

### Local Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/geekpascal/ml-pathloss-predictor.git](https://github.com/geekpascal/ml-pathloss-predictor.git)
    cd ml-pathloss-predictor
    ```

2.  **Install dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

3.  **Run the application:**
    ```sh
    python app.py
    ```

4.  **Access the application:**
    Open your web browser and navigate to `http://127.0.0.1:7860`.

---

## 📖 Usage

### Web Interface

1.  Navigate to the web application in your browser.
2.  Enter the required parameters into the input fields on the form.
3.  Select your desired prediction model (ANN, CNN, or DNN) from the dropdown menu.
4.  Click the "Predict" button to see the calculated path loss.

### API Usage

The application exposes a REST API for programmatic predictions.

#### `/api/predict` (POST)

Send a `POST` request with a JSON payload to get a prediction.

**Example using `curl`:**

```sh
curl -X POST -H "Content-Type: application/json" -d '{
    "model_type": "ann",
    "frequency": 900,
    "distance": 5,
    "tx_height": 30,
    "rx_height": 1.5,
    "environment": "Urban"
}' [http://127.0.0.1:7860/api/predict](http://127.0.0.1:7860/api/predict)
Success Response (200 OK):

JSON

{
  "prediction": 125.45,
  "model_type": "ann",
  "status": "success"
}
/health (GET)
Send a GET request to check the health of the application and see if the models are loaded correctly.

Example using curl:

Bash

curl [http://127.0.0.1:7860/health](http://127.0.0.1:7860/health)
Success Response (200 OK):

JSON

{
    "status": "healthy",
    "models_loaded": ["ann", "dnn", "cnn"],
    "preprocessor_loaded": true
}
📄 License
This project is distributed under the MIT License. See the LICENSE file for more information.
