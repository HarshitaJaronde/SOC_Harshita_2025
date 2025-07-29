**This is a summary of what I have learnt during this project.**

## Text Processing:

- Explored regular expressions as powerful tools for pattern matching and text manipulation, enabling efficient searching, extraction, and modification of text based on specific criteria.

- used NLTK and spaCy for tokenizing text at the sentence, word, and character levels.

- Recognized the importance of text normalization for NLP tasks, including steps such as stopword removal, stemming, lemmatization, accent removal, and case normalization to simplify and standardize input data.

- Implemented part-of-speech (POS) tagging using both NLTK and spaCy.

- Created a word cloud of restaurant compliments using review data to visualize frequently mentioned positive terms.

## Neural Networks:

- Gained foundational knowledge of neural networks, including the role of backpropagation in updating weights and biases.

- Explored gradient descent as an optimization technique for parameter tuning.

- Learned about the argmax and softmax functions for handling multi-class outputs.


## Pytorch:
- Understood PyTorch as a powerful library for building neural networks.

- Built a manual linear model and implemented gradient descent for weight optimization, then transitioned to using PyTorch’s autograd and nn modules for more efficient model creation and training.

- Gained insight into optimizing large numbers of parameters in neural networks

## Recurrent Neural Networks:
- Discovered the effectiveness of RNNs for handling sequential data with variable input and output lengths, thanks to their ability to retain information across time steps.

***Noted the limitations of basic RNNs, such as the vanishing and exploding gradient problems.***

- Trained and tested an RNN model in PyTorch to classify names by country of origin using character-level sequential input, which deepened understanding of hidden layer features and softmax output interpretation.

- Experimented with improving model performance by adjusting the number of epochs and learning rate during optimization.

# Making of the Final Project:

Final Project: Financial News Sentiment + Stock Correlation
Problem: Analyze news sentiment and see its correlation with stock price movements.*
Impact: Helps novice investors understand the impact of news.
Model: LSTM for sentiment + stock data visualization.

Dataset:[Financial Phrasebank] https://www.researchgate.net/publication/251231364

## Processing Files:
->Separated news statements and sentiments from the text files in which they have an '@' delimeter. This required open from io to read files and regex to match the required patttern.

## Making and Saving Vocabulary

-> I made a token counter to contain all the unique words. Tensors will need to be crated based on word indexes. However, there are numerical strings too and their importance must be retained for a stock setiment analysis model. Hence, they are dealt differently. 
 -> Our statement vector would begin with a start of string 'SOS' token and end with an end of string 'EOS' token. The '%' and 'us$' were not added in the counter due to .is_alpha attribute and hence we add them now.

-> We could store the numbers as is but they might clash with words at that index and hence they will be saved with an offset.

## Converting statements and sentiments into tensors:

-> Many of the numbers are floating numbers in our data files and this is why I am creating tensors with dtype=float.32.

-> If an unknown word not present in the vocabulary is encounteres, it can be assigned the index for the UNK_TOKEN

## Designing our neural network:

Since I am using tensors with floating inputs, embedding cannot be used. This is why I will convert the statement tensors into dense matrices with nn.Linear.
These will then be passed as x coordintes for the ReLU activation function.
Then we pass this sequence through LSTM.
Finally, we use the output from the last time step as input to a linear function with three output classes.

## Training:

->I will use Sentences_AllAgree.txt for initial model training to ensure your model learns from the most unambiguous, high-confidence examples.

->Gradually include datasets with lower agreement (75%, 66%, 50%) to increase the diversity and coverage of our training data.

->This exposes the model to more nuanced or ambiguous cases, which can improve its generalization to real-world data.

->After training the model using all three text files, I made a plot showing average loss per epoch for tensors from each of the All_agree, 75_agree and 66_agree text files.

## Stock Data Visualisation:

* We need to visualise how a prediction from this model can be related to the change in stock price.
* I collected some news statements and the corresponding change in the stock price of the company associated with it.
* There is again a preprocess function for differentiating the statementents and the corresponding change.

-> The statements are then converted into tensors such that they can be used as inputs for our model.

***I created a plot showing that a 'neutral' sentiment output from the model corresponded to a change in stock price in range (0-5)% whereas a 'positive' sentiment output corresponded to an increase in of (6-12)%***







