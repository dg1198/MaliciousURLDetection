# Malicious URL Detection with User Authentication

## Overview

Malicious URL Detection is a Flask web application that identifies potentially harmful URLs using a machine learning model. This application includes user authentication features, allowing users to register, log in, and access their profiles securely.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Model Training](#model-training)
- [Dataset](#dataset)
- [API Endpoints](#api-endpoints)
- [User Authentication](#user-authentication)
- [Templates](#templates)
- [Static Files](#static-files)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/MaliciousURLDetection.git
   cd MaliciousURLDetection
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the following model files and dataset, and place them in the project directory:
   - `malicious_url_model.pkl`: The trained machine learning model.
   - `model.pkl`: A backup of the model.
   - `malicious_phish.csv`: The dataset containing over 600,000 URLs and their classifications (malicious or benign).

## Usage

1. Run the application:
   ```bash
   python try(1).py
   ```
2. Access the web application in your browser at `http://127.0.0.1:5000/`.

3. Register a new account or log in to analyze URLs and receive predictions.

## Features

- User-friendly web interface for URL input.
- Predicts whether a URL is benign, phishing, defacement, or malware.
- Provides model performance metrics such as accuracy, precision, recall, and F1 score.
- User registration and login functionality.
- Profile page displaying the username of logged-in users.
- Allows user feedback for model retraining.

## Model Training

The model is trained using the Random Forest algorithm on a dataset of malicious and benign URLs. The dataset is preprocessed, and features such as URL length, number of digits, and domain age are extracted.

## Dataset

The dataset `malicious_phish.csv` contains over 600,000 URLs and labels indicating whether each URL is malicious or benign. This dataset is essential for training the model and is used for initial predictions.

## API Endpoints

- `GET /`: Home page.
- `POST /api/analyze`: Analyzes a URL and returns its prediction.
- `GET /api/metrics`: Returns the model performance metrics.
- `POST /api/feedback`: Accepts user feedback on URL predictions.
- `POST /api/retrain`: Retrains the model using user feedback.

## User Authentication

- **Registration**: Users can create a new account by providing a username and password.
- **Login**: Registered users can log in to access their profile.
- **Profile**: Displays the username of the logged-in user.
- **Logout**: Users can log out securely.

## Templates

The application includes the following HTML templates stored in the `templates` folder:

- **home.html**: The main landing page.
- **about.html**: Information about the application.
- **login.html**: User login page.
- **register.html**: User registration page.
- **profile.html**: Displays the logged-in user's profile.
- **feedback.html**: Page for submitting feedback.
- **index.html**: Page for URL analysis results.

## Static Files

The application includes images and other static files stored in the `static` folder. These are used to enhance the visual appearance of the web pages. You can add or modify images as needed.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
```

