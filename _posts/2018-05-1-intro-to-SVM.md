---
layout: post
section-type: post
title: Intro to SVM (Support Vector Machine)
category: tech
tags:
  - tutorial
published: true
---
A Support Vector Machine (SVM) can be imagined as a surface that defines a boundary between various points of data which represent examples plotted in multidimensional space according to their feature values. The goal of an SVM is to create a flat boundary, called a hyperplane, which leads to fairly homogeneous partitions of data on either side.
SVMs can be adapted for use with nearly any type of learning task, including both classification and numeric prediction. Many of the algorithm's key successes have come in pattern recognition. Notable applications include:

{:refdef: style="text-align: left;"}
• Classification of microarray gene expression data in the field of bioinformatics to identify cancer or other genetic diseases
• Text categorization, such as identification of the language used in a document or organizing documents by subject matter
• The detection of rare yet important events like combustion engine failure, security breaches, or earthquakes
{: refdef}

SVMs are most easily understood when used for binary classification, which is how the method has been traditionally applied.
#### Classification with hyperplanes
SVMs use a linear boundary called a hyperplane to partition data into groups of similar elements, typically as indicated by the class values. For example, the following figure depicts a hyperplane that separates groups of circles and squares in two and three dimensions. Because the circles and squares can be divided by the straight line or flat surface, they are said to be linearly separable.
![ann1.jpg]({{site.baseurl}}/img/ann1.jpg)
The task of the SVM algorithm is to identify a line that separates the two classes. As
shown in the following figure, there is more than one choice of dividing line between
the groups of circles and squares. Three such possibilities are labeled a, b, and c.
How does the algorithm choose?