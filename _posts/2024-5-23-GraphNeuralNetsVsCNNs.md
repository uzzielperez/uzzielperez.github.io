---
layout: posts
title: "Convolutional vs Graph Neural Networks"
categories: Life
author: Uzziel Perez
meta: "Some basic ideas"
math: true
---

This is an evolving note on Convolutional vs Graph Neural Networks from various reading materials.

Convolutional Neural Networks are tailored for grid-like data such as images which is composed of a 2-dimensional grid of pixels. For colored images, each of the pixels has a value that represent the intensity of the red, green and blue or RGB channels. On the other hand, Graph Neural Networks are designed for graph structured data where entries are represented as nodes and the edges represent the relationships between each of them. For our particular project, we are interested in using images as inputs to Graph Neural Networks. But the first step to make is to aggregate or segment pixels into superpixels. The effect of this method reduces the complexity of the image and we capture the spatial relationships in a graph structure.

 
