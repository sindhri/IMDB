# IMDB movie review sentiment classification
Use IMDB movie reviews to classify the sentiment, either positive or negative
Credit: Deep Learning with Python by Jason Brownlee  

## EDA
Shape of the data: 50000 reviews
Unique classes of the predicted variable: [0, 1]
Total number of unique words: 88585
Review length: Mean 234.76 +/- 173 words
![review_length](https://github.com/sindhri/IMDB/blob/master/doc/img1.png)

Parameters:
Maximum unique words: 5000
Maximum length of review: 500 words
Mumber of vectors for word embedding: 32
50/50 split of training and validation

## MLP
![MLP](https://github.com/sindhri/IMDB/blob/master/doc/img2.png)

batch size 128, only 2 epochs is able to reach an accuracy of 87.16%. It only took a minute to run it.

## 1-d CNN
![CNN](https://github.com/sindhri/IMDB/blob/master/doc/img3.png)
Two epochs reached an accuracy of 88.23%, and it only took a minutes to run it.

## Conclusion: 
1-d CNN outperform simple MLP slightly and reached an accuracy of 88.23% with only 2 epoches. Training more epoches will likely to improve the accuracy