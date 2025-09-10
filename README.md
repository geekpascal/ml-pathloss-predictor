---
title: Pathloss App
emoji: 📡
colorFrom: indigo
colorTo: gray
sdk: docker
license: mit
short_description: utilizes ANN, CNN, DNN to accurately predicting pathloss
---

# Pathloss App
 
 A web application for predicting path loss using various machine learning models (ANN, CNN, DNN). The app provides a user-friendly interface for inputting parameters and visualizing results.
 
 ## Features
 
 - Predict path loss using pre-trained models (ANN, CNN, DNN)
 - Simple web interface for user input and result display
 - Model and data pre-processing handled automatically
 - Docker support for easy deployment
 
 ## Project Structure
 
 ```
 app.py                # Main Flask application
 Dockerfile            # Docker configuration
 requirements.txt      # Python dependencies
 models/               # Pre-trained models and preprocessor
 static/style.css      # Custom styles
 templates/            # HTML templates
 ```
 
 ## Getting Started
 
 ### Prerequisites
 
 - Python 3.8+
 - pip
 
 ### Installation
 
 1. Clone the repository:
	 ```
	 git clone <repo-url>
	 cd pathloss-app
	 ```
 
 2. Install dependencies:
	 ```
	 pip install -r requirements.txt
	 ```
 
 3. Run the application:
	 ```
	 python app.py
	 ```
 
 4. Open your browser and go to `http://localhost:5000`
 
 ### Docker
 
 To run with Docker:
 ```
 docker build -t pathloss-app .
 docker run -p 5000:5000 pathloss-app
 ```
 
 ## Usage
 
 - Enter the required parameters in the web form.
 - Select the desired model (ANN, CNN, DNN).
 - View the predicted path loss and related results.
 
 ## File Descriptions
 
 - `app.py`: Main Flask application logic.
 - `models/`: Contains pre-trained models (`.h5`) and preprocessor (`.pkl`).
 - `static/style.css`: Custom CSS for the app.
 - `templates/`: HTML templates for UI.
 
 ## License
 
 This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


