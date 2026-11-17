# IMDB Movie Review Sentiment Analysis using RNN

## Overview
This project uses a Recurrent Neural Network (RNN) built with PyTorch to classify IMDB movie reviews as **positive** or **negative**.

The project covers text preprocessing, TF-IDF vectorization, dataset preparation, RNN model building, training, and evaluation.

## Dataset
- Dataset: IMDB Dataset
- Original records: 50,000
- Records after removing duplicates: 49,582
- Features: Review, Sentiment
- Target classes: Positive and Negative

The dataset is not included in this repository.

## Technologies Used
- Python
- Pandas
- NLTK
- Scikit-learn
- PyTorch

## Project Workflow

### 1. Text Preprocessing
The following preprocessing steps were performed:
- Convert text to lowercase
- Remove URLs
- Remove HTML tags
- Remove punctuation
- Remove stopwords
- Apply stemming using Porter Stemmer
- Encode sentiment labels using LabelEncoder

### 2. Text Vectorization
- Used `TfidfVectorizer` with `max_features=5000`.
- Converted review text into numerical feature vectors.

### 3. Train-Test Split
- 80% training data
- 20% testing data
- `random_state=42`

### 4. RNN Model
Built a simple RNN using PyTorch.

- RNN hidden size: 128
- Number of RNN layers: 1
- Fully connected output layer: 1 neuron
- Sigmoid activation for binary classification

### 5. Model Training
- Loss function: Binary Cross Entropy (`BCELoss`)
- Optimizer: Adam
- Epochs: 10
- Batch size: 64

## Results

**Test Accuracy: 87.06%**

The model classifies movie reviews into positive and negative sentiment categories.

## Key Learnings
- Text preprocessing using NLTK
- Converting text into numerical features using TF-IDF
- Preparing datasets and DataLoaders in PyTorch
- Understanding and implementing a basic RNN
- Training and evaluating a binary classification model

## Conclusion
This project provided practical experience in Natural Language Processing (NLP) and implementing a basic RNN for sentiment classification using PyTorch.
