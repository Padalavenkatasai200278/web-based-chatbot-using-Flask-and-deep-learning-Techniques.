IN THIS README FIRST GO TO CODE WATCH THE INFORMATION (DONT USE PREVIEW TO SEE THE PROCESS)


Web-Based Chatbot Using Flask and Deep Learning


PROJECT STRUCTURE/web-based-chatbot
    /static
        /style
            styles.css

            
    /templates
        index.html
    app.py
    data.json
    training.py
    texts.pkl
    labels.pkl
    model.h5

    
Requirements:---
Python
Keras
NLTK
Flask
HTML/CSS


Overview:---


This project involves creating a web-based chatbot using Flask and deep learning techniques. The chatbot is trained on a dataset (data.json) and uses an artificial neural network (ANN) to classify user messages and generate  responses.



Project Components


data.json: Contains predefined patterns, categories (intents), and responses.
training.py: Python script to build and train the ANN model on the dataset.
texts.pkl: Pickle file storing the vocabulary (list of words).
labels.pkl: Pickle file containing the list of categories (labels).
model.h5: Trained model file with weights and architecture information.
app.py: Flask script to create and run the web-based GUI for the chatbot.
static/style/styles.css: CSS file for styling the web interface.
templates/index.html: HTML file for the web interface layout.
Steps to Create the Chatbot
Import and Load Data:



Create a file named training.py.
Import necessary packages and initialize variables.
Parse the data.json file using the json package to extract patterns, intents, and responses.
Preprocess Data:



Tokenize the text data using nltk.word_tokenize().
Lemmatize words to their base forms and remove duplicates.
Create texts.pkl and labels.pkl to store vocabulary and labels, respectively.
Create Training and Testing Data:



Convert text patterns into numerical data for model training.
Define input (patterns) and output (categories) for training.
Build the Model:



Construct a deep neural network using Keras with three layers.
Train the model for 200 epochs and achieve high accuracy.
Save the trained model as model.h5.
Deploy with Flask:



Create a Flask application in app.py.
Set up the web interface with HTML and CSS in the templates/ and static/ folders.
Load the trained model and pickle files (texts.pkl and labels.pkl).
Implement functions to preprocess user input, predict categories, and retrieve random responses.
