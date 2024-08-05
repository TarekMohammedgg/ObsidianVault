---
date: 2024-07-30
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---

Forward propagation is a key process in neural networks, used to compute the output of the network given an input. It involves passing the input data through the network's layers to obtain the final prediction. Here's a step-by-step overview of how forward propagation works:

### 1. Input Layer

The process begins with the input layer, where the input data (features) is fed into the network.

### 2. Hidden Layers

- Each hidden layer consists of multiple neurons, and each neuron receives input from the previous layer.
- For each neuron in a hidden layer, the input data is multiplied by the neuron's weights and summed. This sum is often referred to as the weighted sum.
- A bias term is added to the weighted sum to shift the activation function. This helps the network model complex patterns more effectively.
- The result is passed through an activation function (e.g., ReLU, sigmoid, tanh) to introduce non-linearity. The activation function's output becomes the input for the next layer.

### 3. Output Layer

The final hidden layer's outputs are passed to the output layer.

- In the output layer, a similar process occurs where the weighted sum and activation function determine the network's final output.
- The output layer's activation function depends on the specific task. For example, a softmax activation is often used for multi-class classification tasks to produce probabilities, while a linear activation might be used for regression tasks.

### Mathematical Representation

For a simple network with one hidden layer:

**Input to Hidden Layer:**





$$ z^{(1)} = W^{(1)} \cdot x + b^{(1)} a^{(1)} = \sigma(z^{(1)}) $$

**Hidden Layer to Output Layer:**



$$ z^{(2)} = W^{(2)} \cdot a^{(1)} + b^{(2)} a^{(2)} = \text{ActivationFunction}(z^{(2)}) $$ 

Where:

- xxx is the input vector.
- W(1)W^{(1)}W(1) and W(2)W^{(2)}W(2) are the weight matrices for the hidden and output layers, respectively.
- b(1)b^{(1)}b(1) and b(2)b^{(2)}b(2) are the bias vectors for the hidden and output layers, respectively.
- zzz represents the weighted sum before applying the activation function.
- aaa represents the output after applying the activation function (activation output).
- σ\sigmaσ is the activation function for the hidden layer.

### Example

Consider a network with a single input neuron, one hidden layer with two neurons, and one output neuron:

**Input Layer:**


$$ Input (x) $$ 

**Hidden Layer:**



$$ z_1^{(1)} = w_{11}^{(1)} \cdot x + w_{12}^{(1)} \cdot x + b_1^{(1)} a_1^{(1)} = \sigma(z_1^{(1)})  z_2^{(1)} = w_{21}^{(1)} \cdot x + w_{22}^{(1)} \cdot x + b_2^{(1)} a_2^{(1)} = \sigma(z_2^{(1)}) $$ 

**Output Layer:**



$$z^{(2)} = w_{1}^{(2)} \cdot a_1^{(1)} + w_{2}^{(2)} \cdot a_2^{(1)} + b^{(2)} a^{(2)} = \text{ActivationFunction}(z^{(2)})$$

Forward propagation continues through all layers until the final output is produced. This output is then used for making predictions, calculating loss, or further processing depending on the specific application.





----
LINKS TO THIS PAGE 
```dataview
LIST FROM ([#](#)) OR outgoing([#](#)) WHERE file.name != this.file.name SORT file.name ASC 
```

