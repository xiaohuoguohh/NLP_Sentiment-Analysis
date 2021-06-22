# NLP_Sentiment-Analysis

For Word Embedding, because the experimental data set is too small, I merge train_data and test_data and added the TED data set as the Word Embedding data.

For Word Embedding, because the experimental data set is too small, the model parameter selects min_count=30 to avoid some rare words that affect the accuracy of semantics and Syntactic.Set epcoh = 10 to get good results and avoid overfitting

For the Word2Vec with SkipGram model, the window size is set to [2,3,5,7,9] and the word vector dimension is set to [10,20,50,100,200] for comparison experiments.

From the results, it can be seen that the semantic accuracy of the Word2Vec with Skipgram model is higher, and it is more in line with the requirements of sentiment analysis. The window size is 3 and the word vector dimension of 50 is the best choice.


<div align=center>
<img width="523" alt="Screen Shot 2021-06-22 at 10 38 41" src="https://user-images.githubusercontent.com/78587287/122856466-6d043e00-d349-11eb-9aec-52f4de895c66.png">
</div>
<div align=center>
<img width="792" alt="Screen Shot 2021-06-22 at 10 38 58" src="https://user-images.githubusercontent.com/78587287/122856493-75f50f80-d349-11eb-902c-88ea33c429a1.png">
</div>   
<div align=center>
<img width="777" alt="Screen Shot 2021-06-22 at 10 38 35" src="https://user-images.githubusercontent.com/78587287/122856587-9fae3680-d349-11eb-97a4-2bb48e21667f.png">
</div>  

For Sequence Model, I tried two models, Bi-RNN and Bi-LSTM. Since the amount of data is small and the selected word vector dimension is only 50, I set the number of features of the hidden layer to 64, and there is only one rnn or lstm layer. The experimental results are shown in result. The final Bi-LSTM model performed better, with a higher F1 score, and trained for 300 epochs with a learning rate of 0.005 to obtain the best results.

<div align=center>
<img width="514" alt="Screen Shot 2021-06-22 at 10 38 12" src="https://user-images.githubusercontent.com/78587287/122856845-1f3c0580-d34a-11eb-9bfe-16c23127b928.png">
</div>  
