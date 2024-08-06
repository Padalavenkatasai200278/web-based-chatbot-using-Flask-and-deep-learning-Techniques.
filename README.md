data.json – The data file which has predefined patterns and responses.
trainning.py – In this Python file, we wrote a script to build the model and train our chatbot.
Texts.pkl – This is a pickle file in which we store the words Python object using Nltk that contains a list of our vocabulary.
Labels.pkl – The classes pickle file contains the list of categories(Labels).
model.h5 – This is the trained model that contains information about the model and has weights of the neurons.
app.py – This is the flask Python script in which we implemented web-based GUI for our chatbot. Users can easily interact with the bot.
static/style/styles.css and html – Designing the web interface .



Here are the 5 steps to create a chatbot :

Import and load the data file
Preprocess data
split the data into training and test
Build the ANN model using keras
Predict the outcomes
Deploy the model in the Flask app

1.Import and load the data file
First, make a file name as trainning.py. We import the necessary packages for our chatbot and initialize the variables we will use in our Python project.
The data file is in JSON format so we used the json package to parse the JSON file into Python. This is how our data.json file looks like.

2. Preprocess data
When working with text data, we need to perform various preprocessing on the data before design an ANN model. Tokenizing is the most basic and first thing you can do on text data. Tokenizing is the process of breaking the whole text into small parts like words.
Here we iterate through the patterns and tokenize the sentence using nltk.word_tokenize() function and append each word in the words list. We also create a list of classes for our tags.
Now we will lemmatize each word and remove duplicate words from the list. Lemmatizing is the process of converting a word into its lemma form and then creating a pickle file to store the Python objects which we will use while predicting.

3. Create training and testing data
Now, we will create the training data in which we will provide the input and the output. Our input will be the pattern and output will be the class our input pattern belongs to. But the computer doesn’t understand text so we will convert text into numbers.

4.Build the model
We have our training data ready, now we will build a deep neural network that has 3 layers. We use the Keras sequential API for this. After training the model for 200 epochs, we achieved 100% accuracy on our model. Let us save the model as ‘model.h5’

5.Predict the response (Flask web-based GUI)
Now to predict the sentences and get a response from the user to let us create a new file ‘app.py’using flask web-based framework.

Note for making flask app we need to make to folders name as static and templates and app.py files.

static folder contains a subfolder with name styles. The styles folder contain css file with the name style.css
Templates folder HTML file with the name of index.html
app.py file for run the flask app using IDE.



We will load the trained model and then use a graphical user interface that will predict the response from the bot. The model will only tell us the class it belongs to, so we will implement some functions which will identify the class and then retrieve a random response from the list of responses.
Again we import the necessary packages and load the ‘texts.pkl’ and ‘labels.pkl’ pickle files which we have created when we trained our model:
To predict the class, we will need to provide input in the same way as we did while training. So we will create some functions that will perform text preprocessing and then predict the class. After predicting the class, we will get a random response from the list of intents.
