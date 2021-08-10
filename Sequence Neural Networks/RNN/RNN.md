# RNN
- Simple NN: 
![image](https://user-images.githubusercontent.com/87144045/128824131-1a3b2215-e796-4755-b28d-f1a1cdd20c3a.png)  
Top view: ![image](https://user-images.githubusercontent.com/87144045/128824188-deddef93-64f1-45ae-9886-aeade8b87f12.png)
- RNN: 
![image](https://user-images.githubusercontent.com/87144045/128824259-f81f6fe3-b533-4dd5-86b3-a30ecf0aae2f.png)
![image](https://user-images.githubusercontent.com/87144045/128824284-20cb5dfd-e50a-4a73-b70e-07f4375fd59e.png)
- The neurons are connecting to themselves through time.
All these neurons have short term memory i.e., what was in the previous neuron or and then one before.
## Forward Propagation and  Backward Propagation:
- Forward Propagation is the way to move from the Input layer (left) to the Output layer (right) in the neural network. The process of moving from the right to left i.e backward from the Output to the Input layer is called the Backward Propagation.
- Forward propagation (or forward pass) refers to the calculation and storage of intermediate variables (including outputs) for a neural network in order from the input layer to the output layer.
- Backpropagation refers to the method of calculating the gradient of neural network parameters.
## The Vanishing Gradient Problem:
- Let's take an example. Suppose we are working with language modeling problem and there are two sequences that model tries to learn:
  - "The cat, which already ate ..., was full"
  - "The cats, which already ate ..., were full"
- What we need to learn here that "was" came with "cat" and that "were" came with "cats". The naive RNN is not very good at capturing very long-term dependencies like this.
- As we have discussed in Deep neural networks, deeper networks are getting into the vanishing gradient problem. That also happens with RNNs with a long sequence size.![16](https://user-images.githubusercontent.com/87144045/128827419-3ce60164-d3bb-4c49-b73f-059052043a0e.png)
  - For computing the word "was", we need to compute the gradient for everything behind. Multiplying fractions tends to vanish the gradient, while multiplication of large number tends to explode it.
  - The gradient keeps on decreasing and it may not be updated properly.(Vanishing Gradients)
  - Exploding gradients can be easily seen when your weight values become NaN.
 ### Solution for this Problem:
 - Exploding Gradient:
   - Truncated Backpropagation
   - Penalties
   - Gradient Clipping
 - Vanishing Gradient
   - Weight Initialization
   - Echo State Networks
   - Long Short-Term Memory Networks (LSTM)
  Reading : [On the difficulty of training recurrent neural networks by Razvan Pascanu (2013)](https://arxiv.org/pdf/1211.5063.pdf)
