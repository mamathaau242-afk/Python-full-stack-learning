# Day 20

## Key Learnings

### Neural Networks 
Are machine learning models inspired by the way the human brain processes information. They consist of interconnected layers of neurons that learn patterns from data and make predictions.
- Learn complex patterns from large datasets.
- Consist of input, hidden, and output layers.
- Used in image recognition, text processing, speech recognition, and prediction tasks.

- x-input
- y-output
- w-weights
- h-hidden layer

### types of output(process)
- one to one(vector to vector)
- one to many(vector to sequence)
- many to one(sequence to vector)
- many to many(sequence to sequence)

### Layers in Neural Network Architecture
- Input Layer: This is where the network receives its input data. Each input neuron in the layer corresponds to a feature in the input data.
- Hidden Layers: These layers perform most of the computational heavy lifting. A neural network can have one or multiple hidden layers. Each layer consists of units (neurons) that transform the inputs into something that the output layer can use.
- Output Layer: The final layer produces the output of the model. The format of these outputs varies depending on the specific task like classification, regression.

### Types of Neural Networks
1. Feedforward Neural Networks(FNN)
Feedforward neural networks are a type of artificial neural network where data flows in one direction from input to output without forming cycles. Inputs pass through hidden layers to produce outputs.
2. Convolutional Neural Networks (CNNs)
Convolutional neural networks are designed to process grid-like data such as images and videos. They use convolutional layers to detect patterns and capture spatial relationships.
3. Recurrent Neural Networks (RNNs)
Recurrent neural network handles sequential data in which the current output is a result of previous inputs by looping over themselves to hold internal state (memory).
4. Generative Adversarial Networks (GANs)
Generative Adversarial Networks consist of two models—a generator and a discriminator that compete with each other. The generator creates synthetic data, while the discriminator distinguishes between real and fake data.
5. Autoencoders (AE)
Autoencoders are feedforward neural networks that learn efficient representations by encoding input data into a latent space and then reconstructing it. The encoder maps the input to a compressed representation, while the decoder reconstructs it.

### Types of Activation Functions
1. Sigmoid Activation Function is characterized by 'S' shape.This formula ensures a smooth and continuous output that is essential for gradient-based optimization methods.
2. Tanh Activation Function 
Tanh function (hyperbolic tangent function) is a shifted version of the sigmoid, allowing it to stretch across the y-axis.
3. ReLU(Rectified Linear Unit)Function 
ReLU activation is defined by A(x)=max(o,x). A(x)=max(0,x), this means that if the input x is positive, ReLU returns x, if the input is negative, it returns 0.
4. Leaky ReLU is similar to ReLU but allows a small negative slope (e.g., 0.01) instead of zero.
5. Softmax Function
Softmax function is similar to ReLU but avoids sharp transitions by being fully differentiable.

