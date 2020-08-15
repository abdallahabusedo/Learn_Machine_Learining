# Learn_Machine_Learining
this is repo is my summary for a machine learning course by Stanford University and Instructor Andrew Ng

# Week 1 

### what is Machine learning ? 
 - Field of study that gives computers the ability to learn without being explicity programming .
 - A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E."
Example: playing checkers.

   - E = the experience of playing many games of checkers
   - T = the task of playing checkers.
   - P = the probability that the program will win the next game.
  
  ### Machine Learning algorithm :
  - Supervised Learning 
  - Unsupervised Learning 
  - Others : 
  
      - Reinforcement Learning 
      - recommender system 
      
      
 # Supervised Learning   
 In supervised learning, we are given a data set and already know what our correct output should look like, having the idea that there is a relationship between the input and the output.
 
### Regression problem
  In a regression problem, we are trying to predict results within a continuous output, meaning that we are trying to map input variables to some continuous function.
  
### classification problem 
  In a classification problem, we are instead trying to predict results in a discrete output. In other words, we are trying to map input variables into discrete categories.
  
 # Unsupervised Learning  
- Unsupervised learning allows us to approach problems with little or no idea what our results should look like. We can derive structure from data where we don't necessarily know the effect of the variables.
- We can derive this structure by clustering the data based on relationships among the variables in the data.
- With unsupervised learning there is no feedback based on the prediction results.
 
 Introduction QUIZ 80% 
 
# Linear Regression with one variable

### Model Representation
![img](http://www.sciweavers.org/tex2img.php?eq=%28x%5Ei%2Cy%5Ei%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)
we’ll use x^(i) to denote the “input” variables also called input features, and y^(i) to denote the “output” or target variable that we are trying to predict

this function h is called a hypothesis. Seen pictorially, the process is therefore like this:

<div align="center">

![image](https://user-images.githubusercontent.com/42722816/90248718-83905d80-de39-11ea-9b86-5f0bc443d896.png)

</div>

### Cost function 
We can measure the accuracy of our hypothesis function by using a cost function. 
This takes an average difference (actually a fancier version of an average) of all the results of the hypothesis with inputs from x's and the actual output y's.

<div align="center">
 
![image](https://user-images.githubusercontent.com/42722816/90249987-a91e6680-de3b-11ea-8465-1aa9af40710c.png)

</div>

This function is otherwise called the "Squared error function", or "Mean squared error". The mean is halved 1/2 as a convenience for the computation of the gradient descent, as the derivative term of the square function will cancel out the 1/2 term.

#### Cost function intuition I
`here we are assuming  that θ=0`

![image](https://user-images.githubusercontent.com/42722816/90252547-fb618680-de3f-11ea-9fe2-c590fb4591a8.png)

![image](https://user-images.githubusercontent.com/42722816/90252803-6d39d000-de40-11ea-9aa0-c43e1b4e883b.png)

When θ1 =1, we get a slope of 1 which goes through every single data point in our model. Conversely, when θ1 = 0.5 we see the vertical distance from our fit to the data points increase.

![image](https://user-images.githubusercontent.com/42722816/90252987-b9851000-de40-11ea-9b2e-1e52083a2962.png)

This increases our cost function to 0.58. Plotting several other points yields to the following graph:

![image](https://user-images.githubusercontent.com/42722816/90252862-86428100-de40-11ea-8cbf-90f61a1ef46e.png)

Thus as a goal, we should try to minimize the cost function. In this case, θ1 = 1 is our global minimum.

#### Cost function intuition II

![image](https://user-images.githubusercontent.com/42722816/90254077-74fa7400-de42-11ea-95f6-72f340d2a819.png)

A contour plot is a graph that contains many contour lines. A contour line of a two variable function has a constant value at all points of the same line. An example of such a graph is the one to the right below.

![image](https://user-images.githubusercontent.com/42722816/90254151-99565080-de42-11ea-94ad-4e908abef78e.png)

The graph above minimizes the cost function as much as possible and consequently, the result of θ1
  and θ0 tend to be around 0.12 and 250 respectively. Plotting those values on our graph to the right seems to put our point in the center of the inner most 'circle'.

### Gradient Descent 

![image](https://user-images.githubusercontent.com/42722816/90254717-7aa48980-de43-11ea-8ff6-5c69a2d01da2.png)

I want to tell you about an algorithm called gradient descent for minimizing the cost function J.


#### Outline 
 - start with some θ0, θ1 (say θ0=0 and θ1=0)
 - keep changing θ0,θ1 to reduce cost function until we hopefully end up at a minimum 
 
#### Gradient descent algorithm 

![image](https://user-images.githubusercontent.com/42722816/90255168-2ea61480-de44-11ea-8156-9803aaf9038a.png)

![image](https://user-images.githubusercontent.com/42722816/90256872-a4ab7b00-de46-11ea-94c1-dc47e98e7e55.png)

#### Gradient descent for Linear regression

![image](https://user-images.githubusercontent.com/42722816/90274970-cfef9380-de61-11ea-910c-b968297841ac.png)

![image](https://user-images.githubusercontent.com/42722816/90276029-830cbc80-de63-11ea-9332-8c0054f09232.png)


Linear Regression with One Variable QUIZ 100%

```
% The ; denotes we are going back to a new row.
A = [1, 2, 3; 4, 5, 6; 7, 8, 9; 10, 11, 12]

% Initialize a vector 
v = [1;2;3] 

% Get the dimension of the matrix A where m = rows and n = columns
[m,n] = size(A)

% You could also store it this way
dim_A = size(A)

% Get the dimension of the vector v 
dim_v = size(v)

% Now let's index into the 2nd row 3rd column of matrix A
A_23 = A(2,3)

```
