# RNN for Spam Message Classification
Overview
This project demonstrates the process of building a simple Recurrent Neural Network (RNN) using Keras and TensorFlow for classifying text messages as either "spam" or "ham" (non-spam). The dataset used for training and testing the model is a CSV file containing labeled messages.

### Requirements
To run this project, you'll need the following Python libraries:

numpy

pandas

sklearn

keras

tensorflow

#### Install the necessary packages using pip:

pip install numpy pandas scikit-learn keras tensorflow

#### Datasets:

label: The label for the message, either spam or ham.

text: The content of the message.

The dataset is split into training and testing sets for model evaluation.

#### Steps
1. Data Preparation
The dataset is read into a Pandas DataFrame and cleaned by removing irrelevant columns.

The labels (spam or ham) are converted to numeric format (1 for spam and 0 for ham).

The text data is split into training and testing sets using train_test_split from sklearn.

2. Data Preprocessing
Tokenization: The text data is tokenized using Keras’ Tokenizer, which converts words into integer sequences.

Padding: The tokenized sequences are padded to ensure all sequences are of equal length (50 in this case), which is necessary for training the RNN.

3. Model Building
Model Architecture:

An Embedding layer is used to convert the tokenized words into dense vectors of fixed size (32 in this case).

An LSTM layer is added to capture long-term dependencies in the text data.

A Dense layer with ReLU activation is used as the output layer.

Recall and Precision: Custom metrics for recall and precision are defined to evaluate the model's performance during training.

4. Model Compilation & Training
The model is compiled using the Adam optimizer and binary cross-entropy loss function. It is then trained on the padded text data.

5. Evaluation
The model's performance is evaluated using accuracy, recall, and precision on the test set.

#### Results
The model aims to classify messages as spam or ham based on the patterns identified during training.
