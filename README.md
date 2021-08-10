# Deep-Learning
My Deep Learning notes and Projects
## Introduction to deep learning

- Single neuron == linear regression
![New doc 10-Aug-2021 11 48 AM_1](https://user-images.githubusercontent.com/87144045/128818214-fbe300f4-769c-44e5-beae-15bcb4f186fe.jpg)
![New doc 10-Aug-2021 11 48 AM_2](https://user-images.githubusercontent.com/87144045/128818288-c18b0d12-efc1-40ea-9e4e-e69429f3dd76.jpg)

- **Activation function:** It defines the output of that neuron given set of inputs. Activation function also helps to normalize the output of any input in the range between 1 to -1. Activation function must be efficient and it should reduce the computation time because the neural network sometimes trained on millions of data points.
  - So, we pass that neuron to activation function to bound output values.
  - Without activation function, weight and bias would only have a linear transformation, or neural network is just a linear regression model.
  - The addition of activation function to neural network executes the non-linear transformation to input and make it capable to solve complex problems such as language translations and image classifications. 
  - **Types of Activation Functions:**
  - Binary step: f(x) = 1 if x > 0  else 0 if x < 0
  -  Linear Activation Function: Y = mZ
  -  RELU(Rectified Linear unit) : Rectified linear unit or ReLU is most widely used activation function right now which ranges from 0 to infinity.All the negative values are converted into zero.
  ![rectified-linear-unit](https://user-images.githubusercontent.com/87144045/128818840-bee00e81-b2dd-4e3f-bcd4-1cc9d68b8a2e.jpg)
  Dying ReLU problem: All the negative values are converted into zero, and this conversion rate is so fast that neither it can map nor fit into data properly which creates a problem
  - Leaky ReLU Activation Function: solves the ‘Dying ReLU’. Leaky ReLU we do not make all negative inputs to zero but to a value near to zero which solves the major issue of ReLU activation function.
  ![](https://lh4.googleusercontent.com/80MrETh1PCKnwG9LzvuwDjKB3RP9E3y8Ghai_lFoaaJiWhrHZ5byujOzYYFVev3vIxoy-ObqjAavFM-aBIcbXVWToMhWu8r8eEEOl8bJdZ-joTIjAlQnbvpzZFmBD7RMtS5JiDRL)
  -  Sigmoid Activation Function: f(x) = 1/(1+e(-x) )  
     used mostly as it does its task with great efficiency, it basically is a probabilistic approach towards decision making and ranges in between 0 to 1, so when we have to make a decision or to predict an output we use this activation function because of the range is the minimum, therefore, prediction would be more accurate.  
  ![](https://lh4.googleusercontent.com/6OrAFufn0HyLY1Rfn36OuZNG-4BRYuFqJyGNTRl6CW0fwFizWK36Nk4uxFfCpxGi5H-8XigIPbXaS9JPCu2TYjbCDnYzZ_qRiIjthfi42sDNcErW9AgNaTroit6CjEknHJxO914J)
  - Hyperbolic Tangent Activation Function(Tanh): This activation function is slightly better than the sigmoid function, like the sigmoid function it is also used to predict or to differentiate between two classes but it maps the negative input into negative quantity only and ranges in between -1 to  1.  
  ![](https://lh6.googleusercontent.com/DcCGRp1XSzCaI8k614tJv_96dSUCiPBbncukrqzsvqhCQlxwubc2iB2xIcBLeXFElHTT1w5ejPkrlV-ye2RKFkJL5l6mzw28fp-T1VBX5Z9Up-3KJcRV9dIz8K3xO_WZ2-F9L3xX)
  - Softmax Activation Function: gives value to the input variable according to their weight and the sum of these weights is eventually one.  
   Softmax is used mainly at the last layer i.e output layer for decision making the same as sigmoid activation works
   ![](https://lh5.googleusercontent.com/IL52WzEWdVcfhpKScPD-pUE3VTDbPjo3Genu5I1REyrdhEQ0HGQulOvdMF2NnEXndQov-h7qKWwheg-2y0O-4Od0AZ16BTp2mZIAHwRRKgGT7NxZzhc2HSgkHYHtxZXUX2RAFpao)  
   For Binary classification, both sigmoid, as well as softmax, are equally approachable but in case of multi-class classification problem we generally use softmax and cross-entropy along with it.
### What is Neural Network?
- Simple NN : This is made of neurons
![](https://raw.githubusercontent.com/ashishpatel26/DeepLearning.ai-Summary/master/1-%20Neural%20Networks%20and%20Deep%20Learning/Images//Others/01.jpg)
- RELU stands for rectified linear unit is the most popular activation function right now that makes deep NNs train faster now.
- Hidden layers predicts connection between inputs automatically, thats what deep learning is good at.
![image](https://user-images.githubusercontent.com/87144045/128820608-01da4062-ae2a-47fa-b62f-35c2c03ef835.png)
- Each Input will be connected to the hidden layer and the NN will decide the connections.
- Supervised learning means we have the (X,Y) and we need to get the function that maps X to Y.
![image](https://user-images.githubusercontent.com/87144045/128820912-8f988072-d45c-4b1e-9685-7cc1a4dab3b3.png)

### Why Neural Networks:
 ![11](https://user-images.githubusercontent.com/87144045/128821041-9adef00e-83ec-4610-af6c-8e27a2930a59.png)
- For small data, NN can perform as Linear regression or SVM (Support vector machine).
- For big data, a big NN is better than a medium NN is better than small NN.
