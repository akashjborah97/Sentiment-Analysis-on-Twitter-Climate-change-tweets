# Sentiment-Analysis-on-Twitter-Climate-change-tweets
Sentiment Analysis is performed on a dataset from kaggle which contains tweets related to Climate change which are categorised into four labels. 
The tweets are extracted and cleaned to convert to lower case, remove unicode characters and remove stopwords. 
These tweets are then vectorized by turning each text into either a sequence of integers using tokenizer. 
After visualizing the length of the tweets, we have set a maxlength and the sequences are padded and truncated with respect to that.
We have prepared a lookup table to view class to index and vice versa.

Our RNN model consists of 4 layers:

Layer 1: Embedding layer to transform input dim=10000 into output dim=64 for a fixed embedding size(maxlen).

Layer 2: Bidirectional sequence-processing layer holding LSTM with 20 number of units which return sequences to return the last output.

Layer 3: Another bidirectional sequence-processing layer holding LSTM with 20 number of units

Layer 4: Dense (fully-connected) layer that transforms the LSTM output into the fixed embedding size with activation function softmax.

The model uses Adam optimizer and measures sparse_categorical_crossentropy loss for the caetegorical data and measures accuracy in sparse_categorical_accuracy. The model predicts the emotion quite well when tested on testing data. 
