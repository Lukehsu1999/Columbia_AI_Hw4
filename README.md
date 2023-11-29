# Columbia_AI_Hw4
Columbia AI Class Homework 4

Name: To-Liang Hsu (th2881)

1. What is one-hot encoding? Why is this important and how do you implement it in keras?
One-hot encoding can help represent categorical variables as numerical values.
It is important because various ML models do not work with categorical data.
In Keras, it's implemented with the to_categorical() method

2. What is dropout and how does it help overfitting?
Dropout is a process of randomly dropping some of the input neurons during training.
This prevents the network from depending too much on specific neurons and make the network more robust.
It helps the network to generalize better and be more strong against noises, thus less vulnerable to overfitting.

3. How does ReLU differ from the sigmoid activation function?
ReLU is easier to calculate, and therefore takes lesser time to train

4. Why is the softmax function necessary in the output layer?
The softmax function scales numbers/logits into probabilities, in our classification problem, this step is vital to calculate the probability and confidence

5. This is a more practical calculation. Consider the following convolution network:
a) input image dimensions = 100x100x1
b) convolution layer with filters-16 and kernel_size=(5,5)
c) MaxPooling layer with pool_size=(2,2) 
What are the dimensions of the outputs of the convolution and maxpooling layers?

Assume stride = 1 and padding = 'same'
Then the output dimension after a Convolutionlayer is [(W-K+2P)/S]+1 =
[(100-5+2*0)/1]+1 = 96
Then the output dimensions are 96*96*16
When going through the maxpooling, the output size = [(W-P)/S}+1 = 
[(96-2)/2]+1 = 48
So after the max-pooling, the output dimensions are 48*48*16

6. Architecture choices
There are two Convolution+Maxpooling layer, extracting 64 /32 features each
The max-pooling is for spatial reduction
I use dropout to help prevent overfitting
