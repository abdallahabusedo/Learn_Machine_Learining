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

