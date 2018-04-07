---
layout: post
section-type: post
title: Machine Learning Terminology
category: Stats
tags:
  - Theory
published: true
---

#### Key ML Terminology
What is (supervised) machine learning? 
{:refdef: style="text-align: left;"}
- ML systems learn how to combine input to produce useful predictions on never-before-seen data.
{: refdef}
#### Labels
A label is the thing we're predicting—the y variable in simple linear regression. The label could be the future price of wheat, the kind of animal shown in a picture, the meaning of an audio clip, or just about anything.
#### Features
A feature is an input variable—the x variable in simple linear regression. A simple machine learning project might use a single feature, while a more sophisticated machine learning project could use millions of features, specified as:
> {X1, X2, ...., Xn}
In the spam detector example, the features could include the following:
{:refdef: style="text-align: left;"}
- words in the email text
- sender's address
- time of day the email was sent
- email contains the phrase "one weird trick."
{: refdef}
#### Models
A model defines the relationship between features and label. For example, a spam detection model might associate certain features strongly with "spam". Let's highlight two phases of a model's life:
{:refdef: style="text-align: left;"}
- Training means creating or learning the model. That is, you show the model labeled examples and enable the model to gradually learn the relationships between features and label.
{: refdef}
{:refdef: style="text-align: left;"}
- Inference means applying the trained model to unlabeled examples. That is, you use the trained model to make useful predictions (y'). For example, during inference, you can predict medianHouseValue for new unlabeled examples.
{: refdef}
#### Regression vs. classification
A regression model predicts continuous values. For example, regression models make predictions that answer questions like the following:
{:refdef: style="text-align: left;"}
- What is the value of a house in California?
- What is the probability that a user will click on this ad?
{: refdef}
A classification model predicts discrete values. For example, classification models make predictions that answer questions like the following
{:refdef: style="text-align: left;"}
- Is a given email message spam or not spam?
- Is this an image of a dog, a cat, or a hamster?
{: refdef}
