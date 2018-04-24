---
layout: post
section-type: post
title: Creating Artificial Neural Network With Python
category: tech
tags:
  - tutorial
published: true
---
#### Scikit Learn
In order to follow along with this tutorial, you'll need to have the latest version of SciKit Learn installed! It is easily installable either through pip or conda, but you can reference the official installation documentation for complete details on this.
#### Data
We'll use SciKit Learn's built in Breast Cancer Data Set which has several features of tumors with a labeled class indicating whether the tumor was Malignant or Benign. We will try to create a neural network model that can take in these features and attempt to predict malignant or benign labels for tumors it has not seen before. Let's go ahead and start by getting the data!
<pre><code data-trim class="c">
{% raw %}
from sklearn.datasets import load_breast_cancer
cancer = load_breast_cancer()
}
{% endraw %}
</code></pre>
This object is like a dictionary, it contains a description of the data and the features and targets:
<pre><code data-trim class="c">
{% raw %}
cancer.keys()
{% endraw %}
</code></pre>
![1.JPG]({{site.baseurl}}/img/1.JPG)
<pre><code data-trim class="c">
{% raw %}
# Print full description by running:
# print(cancer['DESCR'])
# 569 data points with 30 features
cancer['data'].shape
{% endraw %}
</code></pre>
![2.jpg]({{site.baseurl}}/img/2.jpg)
Let's set up our Data and our Labels:
<pre><code data-trim class="c">
{% raw %}
X = cancer['data']
y = cancer['target']
{% endraw %}
</code></pre>
#### Train Test Split
Let's split our data into training and testing sets, this is done easily with SciKit Learn's train_test_split function from model_selection:
Let's set up our Data and our Labels:
<pre><code data-trim class="c">
{% raw %}
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y)
{% endraw %}
</code></pre>
#### Data Preprocessing
The neural network may have difficulty converging before the maximum number of iterations allowed if the data is not normalized. Multi-layer Perceptron is sensitive to feature scaling, so it is highly recommended to scale your data. Note that you must apply the same scaling to the test set for meaningful results. There are a lot of different methods for normalization of data, we will use the built-in StandardScaler for standardization.
<pre><code data-trim class="c">
{% raw %}
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
# Fit only to the training data
scaler.fit(X_train)
{% endraw %}
</code></pre>
![3.JPG]({{site.baseurl}}/_posts/3.JPG)
<pre><code data-trim class="c">
{% raw %}
# Now apply the transformations to the data:
X_train = scaler.transform(X_train)
X_test = scaler.transform(X_test)
{% endraw %}
</code></pre>
#### Training the model
Now it is time to train our model. SciKit Learn makes this incredibly easy, by using estimator objects. In this case we will import our estimator (the Multi-Layer Perceptron Classifier model) from the neural_network library of SciKit-Learn!
![3.JPG]({{site.baseurl}}/_posts/3.JPG)
<pre><code data-trim class="c">
{% raw %}
from sklearn.neural_network import MLPClassifier
{% endraw %}
</code></pre>
Next we create an instance of the model, there are a lot of parameters you can choose to define and customize here, we will only define the hidden_layer_sizes. For this parameter you pass in a tuple consisting of the number of neurons you want at each layer, where the nth entry in the tuple represents the number of neurons in the nth layer of the MLP model. There are many ways to choose these numbers, but for simplicity we will choose 3 layers with the same number of neurons as there are features in our data set:
![3.JPG]({{site.baseurl}}/_posts/3.JPG)
<pre><code data-trim class="c">
{% raw %}
mlp = MLPClassifier(hidden_layer_sizes=(30,30,30))
{% endraw %}
</code></pre>
Now that the model has been made we can fit the training data to our model, remember that this data has already been processed and scaled:
<pre><code data-trim class="c">
{% raw %}
mlp.fit(X_train,y_train)
{% endraw %}
</code></pre>





