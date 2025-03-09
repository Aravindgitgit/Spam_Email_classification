📌 Spam Email Classification using Ensemble Voting Classifier (98% Accuracy)

🔍 Overview

This project focuses on Spam Email Classification using an Ensemble Voting Classifier, achieving 98% accuracy. The model combines multiple machine learning algorithms, leveraging their strengths for more reliable email filtering. The trained model is deployed using FastAPI, enabling real-time spam detection.

🎯 Features

✅ Spam Email Detection – Classifies emails as spam or ham using an ensemble learning approach.✅ Ensemble Voting Classifier – Uses Random Forest, Multinomial Naïve Bayes, SVM, and Gradient Boosting for higher accuracy.✅ FastAPI Web Interface – Allows users to input email content for classification.✅ REST API for Predictions – Users can send email text to receive classification results.✅ Graphical Accuracy Visualization – Displays a graph showing 98% model accuracy.✅ Model Persistence – Trained model is saved and loaded for efficient predictions.

🏗 System Architecture

The project consists of the following components:

1️⃣ Data Collection & Preprocessing – Loads, cleans, and transforms email datasets.2️⃣ Feature Extraction – Converts email text into numerical features using TF-IDF Vectorization.3️⃣ Model Training – Trains an Ensemble Voting Classifier with multiple ML models.4️⃣ Spam Detection API – FastAPI provides an endpoint for real-time email classification.5️⃣ Web UI – A FastAPI-based UI allows users to input email text for classification.6️⃣ Accuracy Graph – Displays 98% model accuracy on the test dataset.

🛠 Tech Stack

Programming Language: Python 🐍

Machine Learning Libraries: Scikit-Learn 🤖

Backend: FastAPI 🚀

Visualization: Matplotlib, Seaborn 📊

REST API Testing: Postman, cURL 🌍

⚙️ Installation & Setup

1️⃣ Clone the Repository

git clone https://github.com/your-username/spam-email-classification.git
cd spam-email-classification

2️⃣ Create a Virtual Environment & Install Dependencies

python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
pip install -r requirements.txt

3️⃣ Run the FastAPI Server

uvicorn main:app --host 0.0.0.0 --port 8000

4️⃣ Access the FastAPI Interface

Once the server is running, open your browser and go to:🔗 http://localhost:8000

API Docs (Swagger UI) are available at:🔗 http://localhost:8000/docs

📊 API Usage Example

Classify an Email as Spam or Ham

Send a POST request to /predict with email content.

cURL Request:

curl -X 'POST'
  'http://localhost:8000/predict'
  -H 'accept: application/json'
  -H 'Content-Type: application/json'
  -d '{"email_content": "Congratulations! You have won a lottery. Click here to claim your prize."}'

Example Response:

{
  "prediction": "Spam",
  "confidence": 0.98
}

📂 Project Structure

├── models/                 # Trained model files
├── static/                 # Sample email datasets
├── main.py                 # FastAPI app
├── model_training.ipynb    # Jupyter Notebook for training & evaluation
├── requirements.txt        # Dependencies
├── README.md               # Project Documentation

🖼 FastAPI UI Preview

📩 Enter Email Content  → 📊 Get Spam Prediction & Confidence Score

📈 Accuracy Graph

The ensemble model achieved 98% accuracy on the test dataset.

🔹 Accuracy vs Epochs:
(Graph showing model performance over epochs)

📌 Future Enhancements

🚀 Dataset Expansion – Train on larger email datasets for improved generalization.🚀 Advanced NLP Techniques – Implement LSTMs or Transformers for better text classification.🚀 Web Dashboard – Build an interactive dashboard for spam trend analysis.
