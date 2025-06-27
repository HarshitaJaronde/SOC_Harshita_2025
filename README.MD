**This is a summary of what I have learnt during this project so far.**

## Text Processing:
Learnt about regular expressions as  tools  used for pattern matching and text manipulation. 
They provide a concise and flexible way to search, extract, and manipulate text from  large data based on specific criteria. 
</br>
Explored nltk and spacy for tokenizing text at sentence, word or character level.
Further, understood imoportance of normalization of text for NLP tasks. Normalization includes steps to  
removing stopwords, stemming , lemmatization, accent removal, case normalization and other steps to make text simpler.

</br>
implementing POS tagging using nltk and spacy.
Creating a wordcloud of compliments to a restaurant using its review data.
</br>

**Converting text to a form that machines can understand (vectors)**
Understood the working of count vectorization as well as TFIDF vectorization by manually making a term-document and term-frequency-document matrix.
Implemented count_vectorizer and TFIDF vecotrizer from sklearn.

***Working principle and importance of Naive Bayes classifier for making predictions based on conditional probabilities***

## Neural Network:
Gained a basic idea of what neural networks do and how backpropagation is the key factor for calculation of wieghts and biases.
**understoood the workng of gradient descent as a tool for optimising parameters**
Learnt about the argmax and softmax functions for dealing with a multi-output layer.

## Pytorch:
I now understand this machine learning library is a powerfool tool in creating a neural network.
I made a manual linear model and a manual algorithm for optimising weights using gradient descent and then used autograd and the NN module for creating a linear model and optimisng weights.
This helped me get an insight into optimising hundreds of parameters that may be present in a neural network.

## Recurrent Neural Netwroks:
They are life-savers when it comes to sequential inputs that may vary in size and outputs that may vary in size too. They accumulate information from previous states instead of just current state for predicting output.

**However, simple RNNs and not used widely due to the vanishing / exploding gradient problem.**

I tried training and testing an RNN model for classifying names into their country of origin by taking sequential character level input using the dataset and nn modules in pytorch.
This helped me understand the role of features in the hidden layer and the sofmax of output tensor. 
We can improve our optimising function by increasing number of epochs and changing value for learning rate.






