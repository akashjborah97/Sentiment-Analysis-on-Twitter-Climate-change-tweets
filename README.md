# Sentiment-Analysis-on-Twitter-Climate-change-tweets
Sentiment Analysis is performed on a dataset from kaggle which contains tweets related to Climate change which are categorised into four labels. 
The tweets are extracted and cleaned to convert to lower case and remove unicode characters. 
These tweets are then vectorized by turning each text into either a sequence of integers using tokenizer. 
After visualizing the length of the tweets, we have set a maxlength and the sequences are padded and truncated with respect to that.
We have prepared a lookup table to view class to index and vice versa.
