[//]: # (Image References)
[image_0]: img/img1.jpg
[image_1]: img/img2.png
[image_2]: img/img3.gif

[eqn1]: img/eqn1.png
[eqn2]: img/eqn2.png

# Control Engineering Lab Report I

The aim of the lab is to understand the *physical models*, *mathematical models* and *state-space equations*. Moreover, understanding of **Simulink** to model our systems in a simulation environment is also covered.

![alt text][image_0]

## Introduction

I'm going to choose **Spring-Mass-Damper** system as an example physical model. Before diving into a simulation environment, I'll first cover the mathematical models of our example system. Then, I'll use Matlab Simulink to model our system in a simulation environment. Also, cover the state-space equations of our system and model those equations in Simulink.

## Spring-Mass-Damper System

![alt text][image_1]

The system we're using here is **Spring-Mass-Damper** system. In the above figure, we could see that **m** is the mass, spring constant **k**, damping ratio **b** and the applied force **f**. We are going to use **Newton's Second Law of Motion** to model our system.

![alt text][image_2]

By adding all the net forces in our system, we can get the following mathematical equation for our system.

<br>

![alt text][eqn1]

![alt text][eqn2]

<br>
Now, we are going to use Matlab Simulink to model our system in a simulation environment.
