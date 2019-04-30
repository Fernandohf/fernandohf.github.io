---
layout: post
title: Real Estate Model, Part 1 - Defining the Problem
---

This is the first post of a series to describe all details present in the creation of a ML model. Each post will focus in a specific step towards the final creation of Machine Learning Model. This first post, will give an overview of the problem we are trying to solve and how to frame it as a Machine Learning problem.

## Summary

List of posts:

1. [Real Estate Model, Part 1 - Defining the Problem]()
2. [Real Estate Model, Part 2 - Getting the Data]()

## Elaborating a Question

![_config.yml]({{ site.baseurl }}/images/01.part1/question.png "Source: <https://undraw.co>")

The creation of a model involves the completion of multiple interconnected tasks. However, a model does not need to be created, if there is no problem to be solved. Generally, it is a good idea to try to formulate the problem as a simple question. In our case, the question is:

>**How much does a real estate cost?**

Take your time to formulate this question, it is really important. This question influences all the next decisions and steps needed to reach our final goal. Try to keep it as simple and direct as possible. At the same time, avoid adding irrelevant description to the final model's output.

## Understanding the Question

![_config.yml]({{ site.baseurl }}/images/01.part1/idea.png "Source: <https://undraw.co>")

Now that we have the question that our model will answer, we need to know how this will be done. For that, let's see where our problem fits in the possible cases of Machine Learning problems. First let's remember some of the common problems that can be solved using ML.

Type of Problem| Description| Question Example
:---|:---|:---|
Classification| Identify to which category an observation belongs| Is this a picture of a cat or dog?
Regression| Estimate a numeric value from a given observation| What is the price of a taxi fare?
Clustering| Group similar observations| Who has similar voting behavior behavior?
Reinforcement Learning| Learn best action based on interaction| How to beat this Mario phase?

It is clear that we have a **Regression Problem**. It is a kind of **Supervised Learning** that uses previous data to predict an numerical output. In our case, the output is the value of the house/property or apartment.

## Answering the Question

![_config.yml]({{ site.baseurl }}/images/01.part1/task.png "Source: <https://undraw.co>")

Now that we know the kind of problem addressed by our model and what is exactly its output, we need to know how the model will learn this task. In a supervised learning problem, **labeled Data** is provided to the model to perform the prediction **task**. Hence, the model needs to map the inputs features to a target variable in a way that minimizes  error or maximizes a **performance metric**. This a good opportunity to fully frame our problem as ML task:

-**Task**: Predict real estate values.
-**Labeled Data**: Listing of apartments/houses/properties and their values.
-**Metric**: The Root Mean Squared Error (RMSE) between target label and predicted values.

## Assumptions

![_config.yml]({{ site.baseurl }}/images/01.part1/assumptions.png "Source: <https://undraw.co>")

With all the preparations ready, you should write down all the assumptions made along the process of solving the problem. For instance, so face this is the indirect assumptions made:

- Features present in the listing are sufficient to estimate the pricing of a real estate.

Right now, this seems like a reasonable assumptions. Nonetheless, later we could see that it is unrealistic or completely wrong. Thus, it is a good practice to list all the indirect and indirect assumption made throughout the model creation process.

Next post, we will discuss how to get relevant data to out problem.

## References

- [Google's ML Crash Course](https://developers.google.com/machine-learning/problem-framing/cases)
- [How to Define Your Machine Learning Problem/](https://machinelearningmastery.com/how-to-define-your-machine-learning-problem/)
