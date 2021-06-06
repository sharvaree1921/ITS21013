# Types of ML:
1. Supervised (mapping is done)
2. Unsupervised (ususally for segregation or testing an AI model)
3. Reinforcement ( punishing if it goes the wrong way XD )

# Neural Networks:
Some important terms:  
- Perceptrons: ( give only 0 or 1, not used)  
- Sigmoid neurons: 
   - give value from 0 to 1.
   - suppose w = vector representing weights, x = inputs or activations, and b = bias, then
   - output: σ(z) = 1/1+exp(-z) where z = w.x + b 
- Cost function:  
   - C(w,b)≡(1/2n)∑(over x)∥y(x)−a∥^2.       ( y(x) is the expected output, a = output given, x is the training input: 784 dimensions)
   - To minimise it, we use 'stochastic gradient descent' which is basically, breaking the large n into small mini-parts and going in the negative direction of gradient.
   - wk→w′k=wk−(η/m)∑(over j)∂CXj/∂wk
- [Code for handwritten digits recognition](https://github.com/mnielsen/neural-networks-and-deep-learning/blob/master/src/network.py)
