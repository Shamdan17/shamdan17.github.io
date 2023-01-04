---
title: "A containerized proof-of-concept implementation of LightChain system"
collection: publications
permalink: /publications/corinfomax
excerpt: #''
date: 2022-11-28
venue: '2022 Conference on Neural Information Processing Systems'
paperurl: #'https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9169463'
citation: #'Ozsoy, S., Hamdan, S.S., Arik, S.Ö., Yuret, D., & Erdogan, A.T. (2022). Self-Supervised Learning with an Information Maximization Criterion. ArXiv, abs/2209.07999.'
---

This article proposes a self-supervised learning method that uses a second-order statistics-based mutual information measure that reﬂects the level of correlation among its arguments and prevents dimensional collapse by encouraging the spread of information across the whole feature space.

For this project, I worked heavily on the technical side of the project, focusing on the implementation, optimizing it, and parallelizing it as well as implementing new ideas and carrying out experiments to test them. I directly contributed to the following:
- Implementing the CorInfoMax self-supervised approach in PyTorch.
- Implementing multi-GPU support for the CorInfoMax loss function and ensuring the exact same performance as in the single GPU case.
- Identified and addressed bottlenecks in dataloading that were heavily affecting performance.
- Identified other improvements in the model implementation and design that led to a two-fold speedup with minimal to no impact in performance.

## Talk

<iframe width="560" height="315" src="https://www.youtube.com/embed/HB_IHzBBRCI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Access

[Access the code and paper here](https://github.com/serdarozsoy/corinfomax-ssl/)

## Recommended citation:

* Ozsoy, S., Hamdan, S.S., Arik, S.Ö., Yuret, D., & Erdogan, A.T. (2022). Self-Supervised Learning with an Information Maximization Criterion. ArXiv, abs/2209.07999.
