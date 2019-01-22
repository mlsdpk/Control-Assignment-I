[//]: # (Image References)
[image_0]: img/img1.jpg
[image_1]: img/img2.png
[image_2]: img/img3.gif
[image_3]: img/img4.png
[image_4]: img/img5.png
[image_5]: img/output_figure1.png
[image_6]: img/output_figure2.png
[image_7]: img/img6.png
[image_8]: img/output_figure3.png

[eqn1]: img/eqn1.png
[eqn2]: img/eqn2.png
[eqn3]: img/eqn3.png
[eqn4]: img/eqn4.png
[eqn5]: img/eqn5.png
[eqn6]: img/eqn6.png

# Control Engineering Lab Report I

The aim of the lab is to understand the *physical models*, *mathematical models* and *state-space equations*. Moreover, understanding of **Simulink** to model our systems in a simulation environment is also covered.

![alt text][image_0]

## Introduction

I'm going to choose **Spring-Mass-Damper** system as an example physical model. Before diving into a simulation environment, I'll first cover the mathematical models of our example system. Then, I'll use Matlab Simulink to model our system in a simulation environment. Also, cover the state-space equations of our system and model those equations in Simulink.

## Spring-Mass-Damper System

<br>

![alt text][image_1]

<br>

The system we're using here is **Spring-Mass-Damper** system. In the above figure, we could see that **m** is the mass, spring constant **k**, damping coefficient **b** and the applied force **f**. We are going to use **Newton's Second Law of Motion** to model our system.

<br>

![alt text][image_2]

<br>

By adding all the net forces in our system, we can get the following mathematical equation for our system.

<br>

![alt text][eqn1]

![alt text][eqn2]

<br>
Now, we are going to use Matlab Simulink to model our system in a simulation environment. Below is the graphical representation of how we'll model our equation in Simulink.

![alt text][image_3]

The following is the actual Simulink blocks representing the above graphical representation.

![alt text][image_4]

We can assign our constants **M**,**k** and **b** to random values in Matlab Command Window.

```
M = 10;
k = 5;
b = 2;
```
Then, we can run our Simulink file and plot the output results of our model. The following is the output results and we can set different values to our model parameters for different result outputs.

![alt text][image_5]

## State-space Equations

We can also use State-Space equations to model our system. The followings are the state-space equations.

![alt text][eqn3]

![alt text][eqn4]

where **A** is an (n x n) system matrix, **x** is a column vector of input variables, **B** is the input matrix, **u** is a column input vector, **C** is an (m x n) matrix of the constant coefficients and **D** is the disturbance matrix.

In order to get matrices A,B,C and D, we can use our mathematical model of Spring-Mass-Damper System. Substituting necessary constants and values into our matrices, we'll get the following state-space equations:

![alt text][eqn5]

![alt text][eqn6]

Now, we can find the response of our system from above state-space equations. We can do that in two different ways. One is to using Matlab built in functions and plot the result. The other way is using Simulink.

Let's focus first in built-in functions way using command line. First, we'll assign our matrices to variables A,B,C and D.

```
% initializing random constant values
F = 1;
m = 10;
k = 5;
b = 2;

% assigning matrices to variables A,B,C and D
A = [0 1; -k/m -b/m];
B = [0 ; F/m];
C = [1 0];
D = 0;
```
Then, we can use Matlab built-in functions to plot our system response.
```
% creating state-space object
sys = ss(A,B,C,D);

% changing state-space eqns to transfer function
G = tf(sys);

% plotting the step response
step(G);
```
![alt text][image_6]

We can see that the step response from state-space equations is the same plot as before. Now, let's use the Simulink blocks to model our state-space equations to get the same output response again. Below is the Simulink model of the open-loop plant.

![alt text][image_7]

Here, I'm using built-in State-Space block to model the open-loop plant and also showing how to make state-space block from scratch. You can see that the output results are the same.

![alt text][image_8]

## Conclusion

Understanding how to approach to get mathematical models from the system, changing state-space equations from the model is essential for control engineers. We can also see that Simulink is very powerful tool. We can use our models and plot our results by using Simulink. We can assign different inputs, different parameters by just clicking the blocks and changing the values.

## Summary

This lab report is written using markdown format. All the mathematical equations are typed in **LaTeX**.

You can find all the Simulink block files at my **Github Repository:**
https://github.com/mlsdpk/Control-Assignment-I

## References

- https://www.codecogs.com/latex/eqneditor.php (LaTeX Online Equation Editor)
- https://www.mathworks.com/discovery/state-space.html
