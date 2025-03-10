# Code Explanation:

The Bag of words model uses TfidfVectorizer to extract the top 1000 words from the text. an MLP model is then trained with one hidden layer. I added a max_iter parameter for convergence. 

The RNN model takes the tokenized text using BERT's tokenizer and padded/truncated to token length of 100. It has 3 layers, 100 hidden units, and embedding size of 100. 

# discussion:

## BoW model:
- train accuracy: 1.0
- test accuracy: 0.8654

achieved perfect training accuracy, but test accuracy is overfitting to the training data. This is common sisnce it's simple and only relies on the frequency of words.

## RNN model:
- train accuracy: improved from 0.8543 to .9830 after 10 epochs
- test accuracy: peaked at 0.8178 in epoch 4, and then fluctuated around 0.8078 in epoch 10. 

The RNN model is more complex and has more parameters to learn. The test accuracy is lower than the BoW model, but not by much. It's more robust and learns sequences and context better. It takes longer to train, but it's more powerful. It can get even better with more epochs and more context (longer sequences).