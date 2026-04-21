---
layout: default
title: 2. Introduction to data science and machine learning
nav_order: 2
parent : Tutorials
---

# Day 2 - Introduction to data science and machine learning
{: .no_toc}

In addition to learning the **basics of programming** and **(interactive) machine learning**, you'll also have to predict the house prices in California (**regression**) and the genre of different songs (**classification**).

For both days of the first bloc you have to fill out an *reflection log* you find here:

[Docx : Reflection Log Template](https://github.com/aica-wavelab/aica-assignments/blob/main/A1_introduction/Reflection-Log-Block1.docx){: .btn .btn-green target="_blank"}

You are encouraged to work in mixed teams! Furthermore, there is homework to do:

[Docx : Homework for HM students](https://github.com/aica-wavelab/aica-assignments/blob/main/A1_introduction/Homework-Block1-HM-Students.docx){: .btn .btn-green target="_blank"}

[Docx : Homework for HMTM students](https://github.com/aica-wavelab/aica-assignments/blob/main/A1_introduction/Homework-Block1-HMTM-Students.docx){: .btn .btn-green target="_blank"}

HMTM students can also do the homework of HM students if they prefer it!

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

## F) Supervised machine learning : A deep dive

### Regression

We take a break from the interactive part and go a little bit more deep into the details. Here we rely on `Pyhton` programming. However, most of the code is just there to be executed and analyzed. To to form groups and explain each other what is actually going on in the notebooks. We do not expect students unfamiliar with coding to be able to code but we expect you to give it a shoot!

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments){: .btn .btn-green
 target="_blank"}

Everything should work on [Google Colab](https://colab.research.google.com/) but if you want you can also run everything on your local machine but you probably have to do some setup. In each notebook in the git repository you find a link that opens the notebook in [Google Colab](https://colab.research.google.com/):

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/4_linear_regression.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

### Classification

We take a break from the interactive part and go a little bit more deep into the details. Here we rely on `Pyhton` programming. However, most of the code is just there to be executed and analyzed. To to form groups and explain each other what is actually going on in the notebooks. We do not expect students unfamiliar with coding to be able to code but we expect you to give it a shoot!

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/5_classification.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

## G) Tutorials in Python

### How to download and launch the tutorials ?

This exercise is part of the homework for HMTM students and optional for HM students.
HM students will receive a different homework which HMTM student can also do instead of theirs.
First go to the github repository of the course:

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments/tree/main/A1_introduction){: .btn .btn-green
 target="_blank"}

There you find different Jupyter notebooks, i.e. files ending with ``.ipynb``.
You can start each notebook by clicking on it and then clicking on the Colab icon.
Alternatively, you can click on the following links to start each notebook in [Google Colab](https://colab.research.google.com/):

+ [1_tutorial_jupyter_notebook.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/1_tutorial_jupyter_notebook.ipynb)
+ [2_1_tutorial_python_variables_operators.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_1_tutorial_python_variables_operators.ipynb)
+ [2_2_tutorial_python_conditions_loops.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_2_tutorial_python_conditions_loops.ipynb)
+ [2_3_tutorial_python_packages.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_3_tutorial_python_packages.ipynb)
+ [2_4_tutorial_python_functions.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/2_4_tutorial_python_functions.ipynb)
+ [3_tutorial_data_science.ipynb](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A1_introduction/3_tutorial_data_science.ipynb)

<!-- 

## G) Recap what you have learned in the lecture

The following [assigment](https://github.com/aica-wavelab/aica-assignments/blob/main/A1_introduction/assigment.pdf) tests your theoretical knowledge of the first block. It is mandatory for all students.

-->

## Submission

Submit your work i.e.:

+ the reflection log
+ your homework

[here](https://syncandshare.lrz.de/preparefilelink?folderID=2Jmzaj6Sx24nh96gohfFN).