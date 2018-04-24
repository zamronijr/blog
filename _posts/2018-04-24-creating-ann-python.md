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
![1.JPG]({{site.baseurl}}/_posts/1.JPG)
<pre><code data-trim class="c">
{% raw %}
# Print full description by running:
# print(cancer['DESCR'])
# 569 data points with 30 features
cancer['data'].shape
{% endraw %}
</code></pre>


