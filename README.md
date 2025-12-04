# **SmartTicket: NLP Support Ticket Classifier**

## ** Project Overview**

SmartTicket is an NLP-powered application designed to automate the categorization of IT support tickets. By analyzing the text of a user's complaint, the model routes the ticket to the correct department (Hardware, Software, Network, or Access).

This project demonstrates **Text Classification**, **Data Preprocessing**, and **Model Deployment** using Python.

## ** Key Features**

* **Text Preprocessing:** Cleaning, Lowercasing, and Punctuation removal.  
* **Vectorization:** TF-IDF (Term Frequency-Inverse Document Frequency) to convert text to numerical features.  
* **Classification:** Logistic Regression for probability-based prediction.  
* **Interactive UI:** Built with Streamlit for real-time inference.

## ** Tech Stack**

* **Python 3.9+**  
* **Scikit-Learn** (Model building)  
* **Pandas** (Data manipulation)  
* **Streamlit** (Web Interface)  
* **Pickle** (Model Serialization)

## ** Project Structure**

├── app.py                \# The main Streamlit web application  
├── generate\_dataset.py   \# Script to generate synthetic training data  
├── train\_model.py        \# Script to train and save the ML model  
├── requirements.txt      \# List of dependencies  
└── README.md             \# Project documentation

## **⚙️ How to Run**

1. **Clone the Repo**  
   git clone \[https://github.com/yourusername/smartticket-nlp.git\](https://github.com/yourusername/smartticket-nlp.git)  
   cd smartticket-nlp

2. **Install Dependencies**  
   pip install \-r requirements.txt

3. Generate Data  
   (Optional: Creates a ticket\_data.csv file)  
   python generate\_dataset.py

4. Train the Model  
   (Creates ticket\_classifier.pkl)  
   python train\_model.py

5. **Run the App**  
   streamlit run app.py

## ** Model Approach**

1. **Data Generation:** Created a synthetic dataset of IT issues using weighted random sampling.  
2. **Preprocessing:** Removed special characters and stop words to reduce noise.  
3. **TF-IDF:** Used to weigh terms; words like "printer" or "wifi" get higher weights than "the" or "is".  
4. **Logistic Regression:** Chosen for its interpretability and efficiency in multi-class text classification.

## ** Future Improvements**

* Implement BERT embeddings for better context understanding.  
* Add a feedback loop to retrain the model on corrected predictions.
