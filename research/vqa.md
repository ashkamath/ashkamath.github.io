---
layout: page
title: Visual Question Answering
permalink: /research/vqa/
---

## Abstract 

This project explored several neural network architec- tures for the Visual Question Answering task [1] which in- volved both the language model and the visual model. In particular, we examined the Convolutional Neural Network, the Long-Short Term Memory network and the Gated Re- current Unit for the language model. For the visual model, we fine tuned the last few layers of VGGNet [16] and ResNet [4]. We also compared different late fusion strategies of the two models. The best architecture we came up with was a Bidirectional-LSTM for questions and the VGGNet features for images, combined by concatenation and MLP (overall accuracy 54.48% on full dataset).

## Introduction

The recent breakthroughs in the field of deep learning have leveraged remarkable advancements in multi-disciplinary Artificial Intelligence (AI) research problems, in particular natural language processing and computer vision problems. For example, the amazing progress made each year in the ILSVRC(Imagenet large scale visual recognition challenge) with new network architectures bringing superior results; the recurrent neural network for text classification, sequence to sequence learning, machine translation and conversation models. However, a complete AI system should be able to solve problems concerning both visual and language models, in addition to being able to perform some kind of common-sense reasoning. This led to some suggestions that Visual Question Answering (VQA) can be used as an alternative well-defined "Visual Turing Test" for modern AI systems.

**Visual Question Answering can be explained as follows: Given an image and a natural language question about the image, the VQA model need to provide an accurate natural language answer which requires solving several sub-problems.** For example, to answer the question *"What is the mustache made of?"* in Figure 1, firstly, the model must have a good understanding of the question (natural language understanding). Then, the model should have some common-sense knowledge that the word *moustache* can be used to refer to objects on the face that are not actually moustaches. Finally, it needs to determine the specific region around the woman's lips and recognize the banana (visual recognition). In addition to (i) multi-modal knowledge requirements, the VQA task also has a (ii) well-defined quantitative evaluation metric to track related research benchmarks, and (iii) it has a well-defined data set and state of art results to compare. For these reasons, the VQA task is an ideal test for a "complete-AI" system.

