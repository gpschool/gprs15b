
# Gaussian Process Summer School, Melbourne, Australia

### 25th-27th February 2015

### Neil D. Lawrence

## Introduction

Welcome to the Gaussian process summer school in Sydney, Australia. 

This notebook provides you with the guide to your lab classes for the entire school. The lab classes are intended to help get you familiar with modeling with Gaussian processes as well as the principles of probabilistic inference.

The lab classes are based on our GPy software, the most recent release was on 21st November 2014. You can install the GPy framework with

```sh
pip install GPy
```

As well as these lab classes there are a range of tutorials on how to use `GPy`, many of which are written by members of my research group. `GPy` is under active development and is released under a BSD license, you'd also be very welcome to contribute!

As well as the GPy software we use our `pods` software for ['open data science'](http://inverseprobability.com/2014/07/01/open-data-science/) for access to data sets and other resources.

```sh
pip install -pre pods
```

## Background 

We will assume background in probabilistic modeling and some familiarity with python and IPython notebook, or Jupyter as it is now known. If you would like to review this material, you can do so with the lab classes below and associated videos.

* [Welcome to `Jupyter`](./jupyter introduction.ipynb) A quick introduction to `Jupyter`, `python` and `numpy`. 
* [Introduction to Probabilistic Regression](./probabilistic interpretations of regression.ipynb) A review of least squares, basis function modelling and the probabilistic interpretation of least squares.
* [Introduction to Bayesian Regression](./bayesian approach to regression.ipynb) Introducing priors over parameters and averaging over solutions.

## Gaussian Processes

The first day will focus on Gaussian process models and developing covariance functions. 
 
* [Introduction to Gaussian Processes](./gaussian process introduction.ipynb) We move from the Bayesian regression with polynomials to Gaussian process perspectives by looking at the priors over the function directly.
* [GPy: Introduction through Covariance Functions](./GPy introduction covariance functions.ipynb) `GPy` is a Python Gaussian process framework that implements many of the ideas we'll see in the course. In this session we introduce its covariance functions and sample from the associated Gaussian processes.
* [Gaussian Process Regression with GPy](./GPy gaussian process regression.ipynb) In this example we show how to do a simple regression model using Gaussian processes in GPy.
* [Optimizing Gaussian Processes](./GPy optimizing gaussian processes.ipynb) The parameters of the covariance function can be optimized. In this example we show how to optimize the parameters of the covariance function. (TODO HMC)

## Structured Outputs with Gaussian Processes

The second day reviews multiple output Gaussian processes for learning vector valued functions and approximations for Gaussian processes.

* [Multiple Output GPs](./multiple outputs.ipynb)
* [TODO Differential Equations and Gaussian Processes](./GP differential equation.ipynb)


## Approximations and Dimensionality Reduction

These examples look at latent variable models and approximations for speeding up inference in Gaussian processes and/or making inference tractable.

* [Low Rank Approximations for Gaussian Processes and the Ceres Data](./Low Rank Gaussian Processes.ipynb)
* [Low Rank Approximations for Gaussian Processes](./low rank approximations.ipynb)
* [Non Gaussian Likelihoods](./non gaussian likelihoods.ipynb)
* [Low Rank and Non Gaussian](./low rank and non gaussian.ipynb)
* [Dimensionality Reduction with Gaussian Processes](./dimensionality reduction with gaussian processes.ipynb) (TODO check0


    
