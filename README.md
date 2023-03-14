# Analysis of Community Support towards Government Policy Using Natural Language Processing
Analysis, data mining and modeling are carried out using a programming language
Python uses free libraries developed open source by the Python community.
Open `requirements.txt` for more complete libraries.

The Selenium library is used for scraping Twitter. The main reason for using selenium is because Twitter's search page is dynamic so it must be simulated like using
web browser. The program will ask for input the username, password, and keyword you want to find, then
The program will simulate scrolling while taking existing tweets up to many tweets that
desirable achieved.

Before it is given to the model, text processing needs to be enforced. Multiple text processing
What is enforced is the removal of links and symbols, generalizing hashtags by giving
space for each capital letter in the hashtag, generalizing abbreviations with mapping abbreviations
words with original words, the use of the stopword dictionary is by deleting common words
(stopword ), and the use of stemmers or the removal of imbuah from the word so as to separate
just the word standard.

Before it is given to the model, text processing needs to be enforced. Multiple text processing
What is enforced is the removal of links and symbols, generalizing hashtags by giving
space for each capital letter in the hashtag, generalizing abbreviations with mapping abbreviations
words with original words, the use of the stopword dictionary is by deleting common words
(stopword ), and the use of stemmers or the removal of imbuah from the word so as to separate
just the word standard.

We plan to create models using a machine learning approach and
deep learning then compares the two to get the best model conclusion.
For machine learning models, TF-IDF vectorization is enforced due to machine inability
learning to understand high-dimensional data. As for the deep learning model, vectorization
Word2Vec was implemented because of our belief in the performance of the pre-trained Word2Vec model on the Indonesian wikipedia dataset

For machine learning, the model to be used XGBoost Regressor that will predict
label values directly (0 for cons, 0.5 for neutral, and 1 for pro). As for
Deep learning algorithm, we use LSTM. There are five LSTM Models that will predict
each label divided into three classes (negative, neutral, positive)

## Test Results and Analysis
Testing is done with data that the model has never seen. Testing using
metrics Mean Absolute Error. From the 20 test data provided, the difference between LSTM and XGB is visible
so clear. The main factor for this performance difference is due to the LSTM combined with
Word2Vec can learn context whereas XGB with TF-IDF can't learn context
sentence

![image](https://user-images.githubusercontent.com/28501206/224891582-51c115a9-f924-4a97-98de-e0c7aafdba56.png)

## Conclusion
Text processing can change model performance significantly. By generalizing from
text processing, the model does not need to choose its own features which of course consume a lot of data and
also time. In terms of architecture, deep learning models are superior in this kind of problem.
Lack of data results in poor model performance. We are quite optimistic if the training data
larger, the model can predict the label well. Pseudo labeling is quite helpful in this
overcome the problem of training data, but overcome it in full. Human intervention
still needed for such cases.
