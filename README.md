[//]: # (Image References)
[image_0]: img/img1.jpg
[image_1]: img/img2.png
[image_2]: img/img3.gif
[image_3]: img/img4.png
[image_4]: img/img5.png
[image_5]: img/output_figure1.png

[eqn1]: img/eqn1.png
[eqn2]: img/eqn2.png

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
