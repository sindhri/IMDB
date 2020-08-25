# IMDB movie review sentiment classification
Use IMDB movie reviews to classify the sentiment, either positive or negative
Credit: Deep Learning with Python by Jason Brownlee  

## EDA
Shape of the data: 50000 reviews
Unique classes of the predicted variable: [0, 1]
Total number of unique words: 88585
Review length: Mean 234.76 +/- 173 words
<img src = "https://github.com/sindhri/IMDB/blob/master/doc/img1.png" width = "500">

Parameters:
Maximum unique words: 5000
Maximum length of review: 500 words
Mumber of vectors for word embedding: 32
50/50 split of training and validation

## Models
### 1. MLP
<img src = "https://github.com/sindhri/IMDB/blob/master/doc/img2.png" width = "500">


batch size 128, only 2 epochs is able to reach an accuracy of 87.16%. It only took a minute to run it.

### 2. 1-d CNN
<img src = "https://github.com/sindhri/IMDB/blob/master/doc/img3.png" width = "500">
Two epochs reached an accuracy of 88.23%, and it only took a minutes to run it.  

### 3. LSTM
<img src = "https://github.com/sindhri/IMDB/blob/master/doc/img4.png" width = "500">

3 epoches, batch size 64  
Much slower
Final accuracy: 87.62%, comparable to previous, but much much much slower, saved

### 4. LSTM with dropout layers
<img src = "https://github.com/sindhri/IMDB/blob/master/doc/img5.png" width = "500">
3 epoches, batch size 64  
Final accuracy: 86.78%, slightly worse

### 5. LSTM with dropout at the concurrent gate
<img src = "https://github.com/sindhri/IMDB/blob/master/doc/img6.png" width = "500">
3 epoches, batch size 64  
Final accuracy: Accuracy: 87.73%, not bad, saved

### 6. LSTM + CNN
<img src = "https://github.com/sindhri/IMDB/blob/master/doc/img7.png" width = "500">
Much faster than LSTM along
Final accuracy: Accuracy: 87.93%, not bad.


## Conclusion: 
1-d CNN outperform simple MLP slightly and reached an accuracy of 88.23% with only 2 epoches. Training more epoches will likely to improve the accuracy