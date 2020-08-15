# Deep_Learning_Tensorflow

This is a very short tutorial of deep learning with tensor flow in which we are converting the temperature scale from degree Celcius to Fahrenheit using tensorflow model.
We have created our model of single dense layer and the "units" in model determine the number of neuron in the model which is related to the internal variable which helps
to tune our model for over thousand or million of iteration and these internal varibales we call them as "Weights" gets updated over each iteration in order to return the
best/optimal outcome according to the trained data.

##### For a single neuron with single input and single output, the internal math looks the same as: y = mx + b and F = 1.8*C + 32 both has the same form.
##### Since the form is same the variables should converges on the standard values of {1.8 and 32}.

We have analyzed the model and as you can see in the program file we have plotted the result as "Number of Epoches" on the X_axis and "Loss mangnitude" on the Y_axis which
clearly shows that as the number of epoches increases the error approaches to Zero.

We can see that by training the model with input data and the corresponding output, the model learned to multiply the input by 1.8 and then add 32 to get the correct result

#### The Training Process
The training process (happening in model.fit(...)) is really about tuning the internal variables of the networks to the best possible values, so that they can map the input to the output. This is achieved through an optimization process called Gradient Descent, which uses Numeric Analysis to find the best possible values to the internal variables of the model

Gradient descent iteratively adjusts parameters, nudging them in the correct direction a bit at a time until they reach the best values. In this case “best values” means that nudging them any more would make the model perform worse

The function that measures how good or bad the model is during each iteration is called the “loss function”, and the goal of each nudge is to “minimize the loss function.”

The training process starts with a forward pass, where the input data is fed to the neural network. Then the model applies its internal math on the input and internal variables to predict an answer.

Once a value is predicted, the difference between that predicted value and the correct value is calculated. This difference is called the loss, and it's a measure of how well the model performed the mapping task. The value of the loss is calculated using a loss function, which we specified with the loss parameter when calling model.compile().

After the loss is calculated, the internal variables (weights and biases) of all the layers of the neural network are adjusted, so as to minimize this loss — that is, to make the output value closer to the correct value.

This optimization process is called Gradient Descent. The specific algorithm used to calculate the new value of each internal variable is specified by the optimizer parameter when calling model.compile(...). In this example we used the Adam optimizer.

Feature: The input(s) to our model.

Examples: An input/output pair used for training.

Labels: The output of the model.

Layer: A collection of nodes connected together within a neural network.

Model: The representation of your neural network.

Dense and Fully Connected (FC): Each node in one layer is connected to each node in the previous layer.

Weights and biases: The internal variables of model.

Loss: The discrepancy between the desired output and the actual output.

MSE: Mean squared error, a type of loss function that counts a small number of large discrepancies as worse than a large number of small ones.

Gradient Descent: An algorithm that changes the internal variables a bit at a time to gradually reduce the loss function.

Optimizer: A specific implementation of the gradient descent algorithm. (There are many algorithms for this. In this course we will only use the “Adam” Optimizer, which stands 
for ADAptive with Momentum. It is considered the best-practice optimizer.)

Learning rate: The “step size” for loss improvement during gradient descent.

Batch: The set of examples used during training of the neural network.

Epoch: A full pass over the entire training dataset.

Forward pass: The computation of output values from input.

Backward pass (backpropagation): The calculation of internal variable adjustments according to the optimizer algorithm, starting from the output layer and working back through each layer to the input.
