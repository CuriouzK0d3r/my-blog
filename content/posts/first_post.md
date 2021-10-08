---
title: How to start with Deep Learning
slug: /start-with-dl
date: 2021-07-10T00:00:00.000Z
tags: ["Deep Learning", "Python" "JavaScript"]
categories: ["Machine Learning"]
description: A description of popular deep learning frameworks
---

# Embracing the hype
Nowadays, everyone is talking about Artificial Intelligence. Whether understands it or not.
This discussion essentially comes down to two terms: Machine Learning and Deep Learning.

**Machine learning** (**ML**) is the study of computer algorithms that improve automatically through experience and by the use of data.

Deep Learning is a type of Machine Learning based on Artificial Neural Networks with multiple layers.

**Artificial neural networks** (**ANNs**) are computing systems inspired by the biological neural networks that constitute animal brains.

Deep Learning is gaining much popularity due to its supremacy in terms of accuracy when trained with a huge amount of data.

I would say you should at least give a try to Deep Learning. It is a quite marketable skill these days.

# A zoo of Deep Learning Frameworks
Every beginner in Deep Learning has to choose the most suitable framework.
Where should you invest your time though?

This post is going to help you get started with DL frameworks.

Frankly, you have many options. But you first need to choose your language.

Most popular choices in this context: JavaScript, Python, and C++.

### JavaScript
This makes sense when you want to train or run your model in the browser.

By far the most popular choice here is [TensorFlow.js](https://www.tensorflow.org/js).
In the past, I have worked on a browser extension that uses Tersorflow.js to produce a verdict about an article’s credibility.
The experience was really good. The main hardships with machine learning in the browser are mostly in the preprocessing libraries rather than in the algorithm itself.

Another good one is [ConvNetJS](https://cs.stanford.edu/people/karpathy/convnetjs/) - but I don’t have much experience using that.

### C++
Obvious benefit: performance.
You will lose some of the convenience of scripting languages, but will also get rid of the overhead.

3 Popular libraries: [Caffe](https://caffe.berkeleyvision.org/), [The Microsoft Cognitive Toolkit](https://docs.microsoft.com/en-us/cognitive-toolkit/) and [Fast Artificial Neural Network Library (FANN)](http://leenissen.dk/fann/wp/).

### Last but not least: Python
Most Data Scientists are using either Python or Matlab and R.

Python has become by far the most widely used language for DL.
4 popular frameworks: [PyTorch](https://pytorch.org/), [TensorFlow](https://www.tensorflow.org/), [Aesara](https://github.com/aesara-devs/aesara) and [Keras](https://keras.io/).

Let’s compare them.

**PyTorch**: 

Developed by Facebook AI, it has a reputation for simplicity, ease of use, flexibility, efficient memory usage, and dynamic computational graphs.

It is one of the easiest to get started with. And it is mostly being used for research.

**Tensorflow**:

Developed by Google, it is known for documentation and training support, scalable production, multiple abstraction levels, and support for different platforms, such as Android.

It has a steeper learning curve and is mostly being used in the industry.

**Keras**:

Keras is an effective high-level neural network API and the easiest for beginners.

This open-source neural network library is designed to provide fast experimentation with deep neural networks, and it can run on top of CNTK, TensorFlow, and Theano.

**Aesara**:

Former project name: Theano.
Theano was developed by the Universite de Montreal and is a foundational library used for DL in Python.

It’s considered the grandfather of deep learning frameworks and has fallen out of favor by most researchers outside academia.

Now the project is abandoned, and the repo points to the Aesara project.

**Features**:

Aesara is suitable for the rapid development of custom operators and symbolic optimizations.

It implements an extensible graph transpilation framework that currently provides compilation via C,  [JAX](https://github.com/google/jax) and  [Numba](https://github.com/numba/numba).

# BONUS - Julia
Julia is a new language for data science that is increasing in popularity.
It is built to provide flexibility and performance. I must say that Julia is optimized for heavy matrix operations.

If you are interested in trying Machine Learning with Julia I would suggest trying [Flux](https://fluxml.ai/), a Machine Learning Stack.

If you want to use Tensorflow there is a Julia wrapper for that, called **TensorFlow.jl**.
The experience will be quite smooth :).
