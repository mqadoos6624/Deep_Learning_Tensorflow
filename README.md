# Deep_Learning_Tensorflow

This is a very short tutorial of deep learning with tensor flow in which we are converting the temperature scale from degree Celcius to Fahrenheit using tensorflow model.
We have created our model of single dense layer and the "units" in model determine the number of neuron in the model which is related to the internal variable which helps
to tune our model for over thousand or million of iteration and these internal varibales we call them as "Weights" gets updated over each iteration in order to return the
best/optimal outcome according to the trained data.

# For a single neuron with single input and single output, the internal math looks the same as: y = mx + b and F = 1.8*C + 32 both has the same form.
# Since the form is same the variables should converges on the standard values of {1.8 and 32}.

We have analyzed the model and as you can see in the program file we have plotted the result as "Number of Epoches" on the X_axis and "Loss mangnitude" on the Y_axis which
clearly shows that as the number of epoches increases the error approaches to Zero.
