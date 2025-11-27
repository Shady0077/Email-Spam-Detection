
# 📧 Spam Email Detector Web Application

This project implements a **Spam Email Detector** using a **Machine Learning model** deployed as a user-friendly web application with **Streamlit**. Users can input a text message, and the application will instantly classify it as either "Spam" or "Not Spam (Ham)."

## ✨ Features

* **Real-time Classification:** Classifies text input as Spam or Ham.
* **Intuitive Interface:** Built with Streamlit for an easy-to-use web interface.
* **Persistent Model:** Uses Python's `pickle` library to load a pre-trained machine learning model.

## 🛠️ Project Structure

The core of the application is typically comprised of:

* `app.py`: The main Python file containing the Streamlit application logic and UI.
* `model.pkl`: The pickled file containing the trained machine learning model (e.g., a Naive Bayes classifier).
* `vectorizer.pkl`: The pickled file containing the fitted text vectorizer (e.g., TF-IDF Vectorizer) used during training.

## 📦 Modules Used

This project relies on the following key Python libraries:

| Module | Description | Role in Project |
| :--- | :--- | :--- |
| **Streamlit** | An open-source Python library for quickly creating and sharing custom web apps for machine learning and data science. | Builds the **web interface** for user input and displaying the classification result. |
| **Pickle** | Used for **serializing and deserializing** Python objects. | Loads the pre-trained ML model and vectorizer from disk (`.pkl` files) into the application memory. |
| **NLTK (Natural Language Toolkit)** | A powerful suite of libraries and programs for symbolic and statistical Natural Language Processing. | Used for **text preprocessing**, such as tokenization, removing stop words, and stemming/lemmatization, before classification. |
| **String** | The standard Python module providing common string operations. | Useful for basic text cleaning and manipulation. |

## 🚀 Getting Started

Follow these steps to set up and run the Spam Email Detector locally.

### 1. Prerequisites

Ensure you have **Python 3.x** installed on your system.

### 2. Installation

Install the required Python packages using `pip`:

```bash
pip install streamlit pandas numpy nltk scikit-learn
````

### 3\. Run the Application

Navigate to the project directory in your terminal and execute the following command:

```bash
streamlit run app.py
```

This command will start the Streamlit server and automatically open the web application in your default browser (usually at `http://localhost:8501`).

-----

## 💡 How It Works

1.  **Model Loading:** The application uses the `pickle` module to load a pre-trained **Machine Learning Model** and its corresponding **Text Vectorizer** (e.g., TF-IDF).
2.  **User Input:** The user enters a text message into the Streamlit text area.
3.  **Preprocessing:** The input text is cleaned and preprocessed using functions that rely on the **NLTK** and **string** modules (e.g., converting to lowercase, removing punctuation, and stemming).
4.  **Vectorization:** The preprocessed text is transformed into a numerical feature vector using the loaded vectorizer.
5.  **Prediction:** The numerical vector is fed into the loaded ML model, which outputs the classification: **Spam** or **Ham**.
6.  **Result Display:** Streamlit displays the final prediction to the user.

<!-- end list -->
