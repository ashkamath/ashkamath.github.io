---
layout: page
title: Domain Adaptation for Sentiment Analysis
permalink: /research/Dom_ad/
---

## Domain Adaptation 

The aim of domain adaptation is to build a classifier such that said classifier trained on a domain (source) can be used to predict in a different domain (target). In particular this can apply to the case where there is plenty of labelled training data available in the source domain and scarce (or no) labelled data in the target domain. When this kind of imabalance is prevalent, good generalisation is very important. In addition, it is often the case that data is distributed very differently in the source and target domains, which presents a major challenge in being able to adapt predictive models.

Supervised machine learning algorithms only perform well when the extensive labelled data is has the same distribution as the test data and the test error of supervised methods generlaly grows proportionately to the distance in distributions between the training and test examples.

In this work we examined two existing methods for unsupervised domain adaptation. Unsupervised here is used in the sense that we do not have labels for the target domain. 


### Stacked Denoising Autoencoders

#### What is aa denoising auto encoder?
An auto-encoder is comprised of an encoder function $$h(·)$$ and a decoder function $$g(·)$$, where typically the dimension of encoder's output is smaller than that of its argument. The "hidden" representation that is obtained after applying the encoder function is usually used as a dimensionally reduced version of the input. The reconstruction of the input by the auto-encoder is given by $$r(x) = g(h(x))$$. Typically, when training an auto encoder one trains it to minimize a reconstruction error pf the form $$loss(x,r(x))$$. A de-noising auto encoder refers to a specific case where the input vector $$x$$ is corrupted into a vector $$\tilde(x)$$ using dropout or random gaussian noise and the model is trained to reconstruct $$x$$ from $$\tilde(x)$$.

