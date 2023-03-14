# Analysis of Community Support towards Government Policy Using Natural Language Processing

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
