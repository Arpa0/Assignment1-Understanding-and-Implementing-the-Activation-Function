# Assignment1-Understanding-and-Implementing-the-Activation-Function
## Task
### 1. Theoretical Understanding
### i) Explain the Activation Function, including its equation and graph.
**Activation Function**

The activation function in neural networks serves to introduce non-linearity into the output of a neuron, allowing the network to learn complex patterns and relationships in the data. It determines whether a neuron should be activated or not based on the weighted sum of its inputs plus a bias term.

**Equation:**

The output or activation (a) of a neuron is calculated using the following equation:

a = f(w1*x1 + w2*x2 + w3*x3 + ... + wi*xi + b)

Where:
- `a` represents the activation of the neuron,
- `f` denotes the activation function,
- `wi` are the weights associated with the respective inputs `xᵢ`,
- `xi` are the input values to the neuron,
- `b` is the bias term.

- ![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/e9b83827-ec1e-4845-97a5-9abee8a9d3d8)



### ii) Discuss why activation functions are used in neural networks, focusing on the role of the activation function.
**Role of Activation Functions in Neural Networks**


Activation functions serve as mathematical gates between the input and output layers in neural networks. They determine whether a neuron will be activated or not, influencing the network's ability to model complex patterns and relationships in data.

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/d10e516f-21b9-4926-87f0-e2aad1511c5b)




**Importance of Activation Functions**

Activation functions play a crucial role in neural networks by introducing non-linearity to the network's computations. Without activation functions, neural networks would only perform linear transformations on inputs using weights and biases, resulting in a stack of linear regression models. This limitation severely restricts the network's ability to learn complex tasks and patterns.



**Functionality of Activation Functions**

In a neural network, activation functions are applied at each layer during forward propagation. This introduces non-linear transformations, enabling the network to learn and model intricate relationships within the data. By adding non-linearity, activation functions enhance the network's capacity to handle complex tasks and improve its performance.


### 2. Mathematical Exploration
### i) Derive the activation function formula and demonstrate it's output range

**Activation Functions and Output Range**


**Sigmoid Activation Function** 

The sigmoid function takes any real value as input and outputs values in the range of 0 to 1.

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/a4a1de00-579b-4ca1-bc47-673b6a0a9c09)

It's represented mathematically as: 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/56767595-075f-4d30-89d4-b26336eaadfa)


This equation represents a logistic curve, where x is the input to the function. The exponential term e^-x

 ensures that the output is bounded between 0 and 1.


 **Tanh Function (Hyperbolic Tangent)**

 Similar to the sigmoid function, the tanh function outputs values in the range of -1 to 1. 


 ![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/2605ab5f-fe41-4949-be7a-77444c810b30)

 Mathematically, it's expressed as:

 ![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/ece51643-a265-472d-ae33-755a2cda99b4)


 Here, the numerator e^x−e^−x and denominator e^x+e^−x represent the hyperbolic tangent function, which compresses the input values into the range of -1 to 1.

**ReLU Function (Rectified Linear Unit)**

The ReLU function is defined as the positive part of its argument. It outputs the input value if it's positive, and zero otherwise.

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/696dae9e-7428-42bb-91d7-756c5a812443)

 Mathematically: 

 ![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/2321a8b5-f49f-4060-9d2a-578bfe0146aa)

 
This equation indicates that the output of the ReLU function is zero for negative inputs, and equal to the input value for non-negative inputs.


**Leaky ReLU Function**

The leaky ReLU function is an improvement over the ReLU function, introducing a small positive slope for negative inputs to avoid the "dying ReLU" problem. 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/71b369ce-490b-4b24-958d-c66a1af24120)

 
It's defined as: 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/c456ce3b-0f3a-42d7-8e5a-7c8115cc22b7)


 
Here, if the input x is negative, the output is a fraction (0.1) of the input value, otherwise, it's equal to the input value.



**Exponential Linear Units (ELUs) Function**

ELU modifies the slope of the negative part of the function using an exponential curve.


![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/37b556d7-ef48-4250-a092-110e0a6b3453)


 
 It's represented as: 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/d9b14ddc-4904-4c9b-a62c-1fe323c8dd4c)

 
For non-negative inputs, the output is equal to the input value, while for negative inputs, it's a function of the exponential term e^x minus one.


**Softmax Function**

Softmax function calculates the relative probabilities of different classes, ensuring that the sum of all probabilities equals 1.

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/101b4c65-474f-4c13-93f1-aacdb63bb909)

 
 Mathematically: 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/828d21a5-6ed5-4742-848a-cf3369f66812)

 
Here, zi represents the input to the softmax function, and the denominator ensures that the output probabilities sum up to 1.


**Swish Function**

Swish is a self-gated activation function that outperforms ReLU in various domains. 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/145debee-3ccf-4e89-9a71-f501d226cebb)

 
It's defined as: 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/a7a82c1a-8b44-4a37-a9c7-0bd15f9df793)

 
The function is bounded below but unbounded above, with the output approaching a constant value as x approaches negative infinity, and approaching infinity as x approaches positive infinity.


### ii) Derivative of Activation Functions and Significance in Backpropagation
**Sigmoid Activation Function**

The derivative of the sigmoid function  is calculated as:

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/66c55fd0-4dd2-4fd8-9cc4-160dcb8da754)


In the context of backpropagation, the derivative of the sigmoid function is crucial for adjusting the weights during training. It helps in determining the magnitude and direction of the weight updates based on the error signal propagated backwards through the network.


**Tanh Function (Hyperbolic Tangent)**
The derivative of the hyperbolic tangent function:

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/4fcc5e97-c153-453f-aa50-f71493fe59af)

Similar to the sigmoid function, the derivative of the tanh function plays a vital role in backpropagation, enabling the network to learn from errors and adjust the weights accordingly.


**ReLU Function (Rectified Linear Unit)**

The derivative of the ReLU function:

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/df12f6aa-419f-4487-9c3a-36538de468b5)


In backpropagation, the derivative of the ReLU function is essential for determining which neurons contribute to the error signal and guiding the weight updates accordingly.


**Leaky ReLU Function**

The derivative of the leaky ReLU function:

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/399dc8a5-25fc-4256-bd2a-3fb2c3651912)


The derivative of the leaky ReLU function is similar to ReLU but introduces a small slope for negative inputs, preventing neurons from becoming completely inactive during training.

**Exponential Linear Units (ELUs) Function**

The derivative of the ELU function is: 

![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/4db9156e-e607-44a0-b5e9-53118dbf01ca)

In backpropagation, the derivative of the ELU function helps in adjusting the weights to minimize the error by providing information about the rate of change of the activation function with respect to its input.

The derivatives of activation functions are vital in the backpropagation process as they provide information about the rate of change of the activation function with respect to its input, guiding the adjustment of weights to minimize the error and improve the performance of the neural network.


### 3. Programming Excercise
### Create a small dataset and implement the activation function.

The implementation of the activation functions is done in the "Activation Function.py" file. For the sake of simplicity and better understanding, I have chosen the sigmoid, tanh, and ReLU activation functions.


The output of the implemented code is given below:


![image](https://github.com/Arpa0/Assignment1-Understanding-and-Implementing-the-Activation-Function/assets/73717696/9428a167-a12e-4641-a91c-63fa7200a654)


**Analysing output for sigmoid activation function**


The sigmoid function, also known as the logistic function, transforms the input values into a range between 0 and 1. For the generated dataset, the sigmoid function squashes the input values to the interval [0, 1]. As the input values move towards positive infinity, the sigmoid output approaches 1, and as they move towards negative infinity, the output approaches 0. This behavior is evident in the sigmoid plot, where the values are squeezed towards the extremes of the range, exhibiting a characteristic S-shaped curve.


**Analysing output for hyperbolic tangent (tanh)  function**


The hyperbolic tangent (tanh) function is similar to the sigmoid function but maps the input values to the range [-1, 1]. In the context of the generated dataset, the tanh function compresses the input values to lie within the interval [-1, 1]. As with the sigmoid function, positive input values yield positive outputs close to 1, and negative input values yield negative outputs close to -1. The tanh plot displays a symmetric curve around the origin, reflecting this behavior.


**Analysing output for Rectified Linear Unit (ReLU) function**

The Rectified Linear Unit (ReLU) function is a piecewise linear function that returns zero for negative input values and the input value itself for positive input values. In the dataset, ReLU acts as a threshold function, setting negative input values to zero while leaving positive input values unchanged. As a result, the ReLU plot displays a linear increase for positive input values, while negative input values are flattened to zero. This characteristic makes ReLU particularly useful for introducing sparsity and promoting sparse representations in neural networks.


### 4. Analysis
### i) Advantages and Disadvantages of Activation Functions in Neural Networks
### Sigmoid / Logistic Activation Function


***Advantages***

Suitable for models predicting probabilities due to its range limitation between 0 and 1.
Provides a smooth gradient, aiding in stable convergence during training.


***Disadvantages***


Suffers from vanishing gradient problem, particularly in deep networks, which can hinder learning.


### Tanh Function (Hyperbolic Tangent)

***Advantages***


Outputs are zero-centered, facilitating easier mapping of output values.
Useful for hidden layers as it helps in centering the data around zero, simplifying subsequent layer learning.


***Disadvantages***


Faces vanishing gradient problem similar to sigmoid function.
Steeper gradient than sigmoid, leading to potential issues with gradient explosion.


### ReLU Function (Rectified Linear Unit)


***Advantages***


Computationally efficient due to activation of only a subset of neurons.
Accelerates convergence of gradient descent, enhancing training speed.


***Disadvantages***


Prone to the Dying ReLU problem, where neurons can become inactive and hinder learning.
Negative inputs immediately zeroed out, impacting model's ability to capture negative correlations in data.


### Leaky ReLU Function

***Advantages***

Addresses Dying ReLU problem by allowing for non-zero gradient for negative inputs.


***Disadvantages***

Inconsistent predictions for negative inputs.
Small gradient for negative values can slow down learning.

### Exponential Linear Units (ELUs) Function

***Advantages***

Smooth transition for negative inputs, avoiding abrupt changes in gradient.
Mitigates dead ReLU problem by introducing a curve for negative values.


***Disadvantages***

Increased computational time due to exponential operation.
Fixed 'α' parameter, limiting adaptability to different datasets.

### Swish Function

***Advantages***

Smooth and non-monotonous, enhancing expression of input data and weights.
Retains relevance of small negative values and sparsity, contributing to better learning.


***Disadvantages***

Limited exploration in comparison to other functions.
May require additional computational resources due to its non-linear nature.


### ii) Impact of Activation Function on Gradient Descent and Vanishing Gradients

Activation functions play a crucial role in determining the behavior of gradient descent during training in neural networks, particularly in addressing or exacerbating the problem of vanishing gradients. Here's a discussion on their impact:


***Effect on Gradient Descent***


Activation functions influence the shape of the loss function's surface, affecting the convergence of gradient descent.
Smooth activation functions, such as sigmoid and tanh, provide a continuous and differentiable surface, aiding gradient descent convergence.
Non-smooth activation functions, like ReLU and its variants, can introduce discontinuities in the loss surface, potentially slowing down convergence or causing instability during training.


***Vanishing Gradients***



Vanishing gradients occur when the gradients become extremely small as they propagate backward through the layers of a deep neural network during training.
This phenomenon is particularly problematic with sigmoid and tanh activation functions, as their derivatives tend to approach zero for large or small inputs, causing gradients to vanish as they propagate through multiple layers.
As a result, the weights of early layers receive little to no updates, impeding the learning process and limiting the network's ability to capture complex relationships in the data.
The problem of vanishing gradients can lead to long training times, poor convergence, and suboptimal performance, especially in deep networks.



***Addressing Vanishing Gradients***
One approach to mitigate vanishing gradients is to use activation functions that have gradients that do not approach zero or do so less rapidly for extreme input values.
Rectified Linear Unit (ReLU) and its variants, such as Leaky ReLU and Parametric ReLU, have been found to alleviate the vanishing gradient problem to some extent by providing non-zero gradients for positive inputs.
Exponential Linear Units (ELUs) also offer a solution by introducing a smooth transition for negative inputs, preventing gradients from vanishing too quickly.



