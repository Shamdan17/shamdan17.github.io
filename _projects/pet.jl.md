---
title: "It's Not Just Size That Matters: Small Language Models Are Also Few-Shot Learners"
excerpt: "A replication of PET, achieving better performance than GPT-3 with 1% of the parameters and only 32 training samples."
collection: projects
permalink: /projects/petjl
date: 2020-09-15
categories:
  - University Project
tags:
  - Deep Learning
  - Knet
  - Few Shot Learning
  - NLP
  - Transformers
---

## Code

The code is available on github [here](https://github.com/Shamdan17/pet.jl/).

## Skills

* Transformers
* Few shot learning
* Julia
* Knet

## About

This project was part of the COMP541 Deep Learning course at Koç University.

In this project I replicated the paper by [Schick et al.](https://arxiv.org/abs/2009.07118). 

Working with Knet, a deep learning framework developed by Prof. Deniz Yuret at Koc University, I had to implement everything from scratch. This meant I had to delve deep into the implementation of every single step of the model, understand it, and know how to replicate it in terms of simple operations supported by Knet.

During this project, I had to learn about the inner workings of and implement:
- [ALBERT](https://arxiv.org/abs/1909.11942), a transformer encoder which utilizes extreme weight sharing to deliver good performance at a low number of parameters.
  - Parallelized multihead attention
  - Layer normalization
- AdamW, a version of Adam with weight decay
  - One problem introduced by adding a weight decay regularization term to the loss function is that it leads to undesireable behavior when the optimizer uses first or second moments of the gradient.
  - AdamW solves this problem by incorporating the weight decay into the optimizer itself, without having to add a loss term that affects the first/second moment calculations.
- Different learning rate schedulers
  - I implemented an elegant interface for learning rate schedulers that fits right into the optimization pipeline of Knet and that does not require much modification to use.
- GELU
  - Knet had no support for GPU for activation functions like GELU so I implemented a GPU-compatible version of GELU.

I have heavily optimized the model, and the Knet implemented ended up being faster than the original PET implementation when used on the same machines.