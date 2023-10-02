# Sentiment_Analysis

This project was a part of my internship at CodeClause

The dataset was taken from Kaggle and at first EDA (Exploratory Data Analysis ) performed in order to check any outliers, since data is too large to be handled on a CPU-based machine, so that's why I performed sentiment analysis on the first 500 samples of the dataset, that was more on the positive side as also seen from the graph. 


In short, I have utilized 3 different methods or models to do sentiment analysis:


1.  VADER (Valence Aware Dictionary and sEntiment Reasoner)


-Working: It removes the stop words and each individual word is given a score depending on the sentiment and then the total sentiment score of a particular sentence is determined by combining all words score. It can with the help of nltk's SentimentIntensityAnalyzer(), but one constraint is that it doesn't account for the context of the words.


2.  Roberta Pre-trained model:


-Working: It is a transformer-based deep learning model from a hugging face platform. The model that I used was pre-trained on large Twitter data for sentiment analysis and the benefit of this is that rather than training the model again which consumes time and resources we can just do transfer learning by utilizing the trained weights and applying them to our dataset to see the outputs. It also accounts for the context of the words.


3. Hugging face Transformer's pipeline:


-Working: This is a game changer approach as just by importing the pipeline and allocating the task of our need it automatically installs the default model and embedding for this pipeline according to the task and then it can be applied to the dataset similar to shown in the video.


Results: The results from the Roberta model were better than the VADER model as it was more confident regarding its sentiment scores and ratings as compared in the graph using Seaborn's pair plot. Further, the last method was implemented to show the convenience of using the pipeline.
