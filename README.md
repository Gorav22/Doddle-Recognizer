# Doodle Recognizer (MERN + Flask)

This project implements a doodle recognizer using a combination of MERN (MongoDB, Express.js, React.js, Node.js) for the frontend and backend, and Flask (Python) for the machine learning model serving. It allows users to draw doodles in a web interface, which are then classified by a machine learning model.

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Architecture](#architecture)
* [Installation](#installation)
* [Usage](#usage)
* [Data](#data)
* [Model](#model)
* [Contributing](#contributing)
* [License](#license)

## Overview

The Doodle Recognizer provides a web-based interface for users to draw doodles and receive real-time classifications. The application leverages a MERN stack for the user interface and data handling, while a Flask API serves the machine learning model for doodle recognition.

## Features

* Interactive doodle drawing interface using React.
* Real-time classification of doodles.
* MERN stack for frontend and backend data management.
* Flask API for machine learning model serving.
* [Mention specific categories of doodles that are recognized, e.g., circles, squares, triangles, etc.].
* [If the user can save their doodles, mention that]

## Architecture

The application follows a distributed architecture:

* **Frontend (React.js):**
    * Provides the user interface for drawing and displaying results.
    * Communicates with the Express.js backend for data handling.
    * Communicates with the Flask api for prediction results.
* **Backend (Express.js/Node.js):**
    * Handles user requests and data storage (MongoDB).
    * Serves as an API for the React frontend.
* **Machine Learning API (Flask/Python):**
    * Hosts the trained machine learning model.
    * Receives doodle images from the frontend.
    * Performs classification and returns results.
* **Database (MongoDB):**
    * Stores user data and doodle history (if implemented).

## Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/Gorav22/Doddle-Recognizer.git
    cd  Doddle-Recognizer
    ```

2.  **Install dependencies:**

    * **Frontend (React.js):**

        ```bash
        cd frontend
        npm install
        ```

    * **Backend (Express.js/Node.js):**

        ```bash
        cd backend_node
        npm install
        ```

    * **Machine Learning API (Flask/Python):**

        ```bash
        cd backend_node
        pip install -r requirements.txt #Or conda install if using conda
        ```

3.  **Set up MongoDB:**

    * Install and run MongoDB.
    * Update the database connection string in `backend_node/.env` (create if it doesn't exist).

4.  **Download the machine learning model:**

    * Place the trained model in the `backend` directory.

5.  **Configure Environment Variables:**

    * Create a `.env` file in the server directory and add any needed environment variables.

## Usage

1.  **Start the backend:**

    ```bash
    cd backend_node
    npm run start #or npm start
    ```

2.  **Start the frontend:**

    ```bash
    cd frontend
    npm run dev
    ```

3.  **Start the Flask API:**

    ```bash
    cd backend
    python app.py
    ```

4.  **Open the application in your browser:**

    * Navigate to `http://localhost:5173` (or the appropriate port).
    * Draw a doodle, and click the "Recognize" button.

## Data

* [Describe the dataset used for training the model. If you created the dataset, explain how it was collected.]
* [If the dataset is publicly available, provide a link.]
* [Mention any preprocessing steps performed on the data.]

## Model

* [Describe the machine learning model used (e.g., Convolutional Neural Network).]
* [Explain the training process, including hyperparameters and evaluation metrics.]
* [Mention how the Flask API processes the doodle image and returns the classification result.]
* [If the model is pre-trained, mention its accuracy and performance.]
* [If applicable, mention how to train the model yourself]

## Contributing

Contributions are welcome! Please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and commit them.
4.  Push your changes to your fork.
5.  Submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more information.