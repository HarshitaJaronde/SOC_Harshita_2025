**This is a summary of what I have learnt during this project so far.**

## Text Processing:

- Explored regular expressions as powerful tools for pattern matching and text manipulation, enabling efficient searching, extraction, and modification of text based on specific criteria.

- used NLTK and spaCy for tokenizing text at the sentence, word, and character levels.

- Recognized the importance of text normalization for NLP tasks, including steps such as stopword removal, stemming, lemmatization, accent removal, and case normalization to simplify and standardize input data.

- Implemented part-of-speech (POS) tagging using both NLTK and spaCy.

- Created a word cloud of restaurant compliments using review data to visualize frequently mentioned positive terms.

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






