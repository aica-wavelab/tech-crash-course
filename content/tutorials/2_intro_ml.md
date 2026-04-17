---
layout: default
title: 2. Introduction to data science and machine learning
nav_order: 2
parent : Tutorials
---

# Day 2 - Introduction to data science and machine learning
{: .no_toc}

---

## Table of contents
{: .no_toc .text-delta }

2. TOC
{:toc}

---

## Introduction

In our second day, we start with a challenge: Play a game of Snake without using the mouse or keyboard!

Afterwards we will interrupt the interactive part of the course and go deeper into the theory of machine learnin by working on jupyter notebooks using [Google Colab](https://colab.research.google.com/).

## E) Hands-on Challenge : Snake with Teachable Machine

### Warm-up

Go to [Teachable Machine](https://teachablemachine.withgoogle.com/) and train another image classifier to recognize different items you have with you.
Export it such that you can use it inside p5.js. It works very similar to [Marcelle](https://marcelle.dev/).
Go to [Teachable Machine Sketch](https://editor.p5js.org/BZoennchen/sketches/TZMLo1lpr) and use your trained model in this sketch.

### Controlling Snake with your camera

The following is a [p5js sketch](https://editor.p5js.org/BZoennchen/sketches/TqlpdVLq9) of the well-knwon game called Snake.
Start the sketch and play a game.
Next your task is to train an image classifier with [Teachable Machine](https://teachablemachine.withgoogle.com/) to play the game using your camera input as control source.
After training you should be able to control the game with poses of your body.

### Expand the players

Can you make the game work for different people?

### The challenge

Each team plays a game in front of the class. The team with the most points wins!


## F) Regression : A deep dive

We take a break from the interactive part and go a little bit more deep into the details. Here we rely on `Pyhton` programming. However, most of the code is just there to be executed and analyzed. To to form groups and explain each other what is actually going on in the notebooks. We do not expect students unfamiliar with coding to be able to code but we expect you to give it a shoot!

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments){: .btn .btn-green
 target="_blank"}

Everything should work on [Google Colab](https://colab.research.google.com/) but if you want you can also run everything on your local machine but you probably have to do some setup. In each notebook in the git repository you find a link that opens the notebook in [Google Colab](https://colab.research.google.com/):

<img src="{{ '/assets/images/colab-icon.png' | relative_url }}" alt="Google Colab Icon">

[Regression on Google Colab](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/4_linear_regression.ipynb){: .btn .btn-green target="_blank"}

## F) Classification : A deep dive

We take a break from the interactive part and go a little bit more deep into the details. Here we rely on `Pyhton` programming. However, most of the code is just there to be executed and analyzed. To to form groups and explain each other what is actually going on in the notebooks. We do not expect students unfamiliar with coding to be able to code but we expect you to give it a shoot!

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments){: .btn .btn-green
 target="_blank"}

Everything should work on [Google Colab](https://colab.research.google.com/) but if you want you can also run everything on your local machine but you probably have to do some setup. In each notebook in the git repository you find a link that opens the notebook in [Google Colab](https://colab.research.google.com/):

<img src="{{ '/assets/images/colab-icon.png' | relative_url }}" alt="Google Colab Icon">

[Classification on Google Colab](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/5_classification.ipynb){: .btn .btn-green target="_blank"}

## G) Tutorials in Python

### How to download and launch the tutorials ?

#### Using Google Colab

First go to the github repository of the course:

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments/tree/main/A1_introduction){: .btn .btn-green
 target="_blank"}

There you find 6 different Jupyter notebooks, i.e. files ending with ``.ipynb``.
You can start each notebook by clicking on it and then clicking on the Colab icon.
Alternatively, you can click on the following links to start each notebook in Google Colab:

+ [1_tutorial_jupyter_notebook.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/1_tutorial_jupyter_notebook.ipynb)
+ [2_1_tutorial_python_variables_operators.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_1_tutorial_python_variables_operators.ipynb)
+ [2_2_tutorial_python_conditions_loops.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_2_tutorial_python_conditions_loops.ipynb)
+ [2_3_tutorial_python_packages.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_3_tutorial_python_packages.ipynb)
+ [2_4_tutorial_python_functions.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_4_tutorial_python_functions.ipynb)
+ [3_tutorial_data_science.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/3_tutorial_data_science.ipynb)