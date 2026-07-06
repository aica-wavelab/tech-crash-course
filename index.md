---
layout: default
title: About
nav_order: 1
description: "Description of the AICA crash course on Human-AI interaction (Summer Semester 2026)"
permalink: /
---

# AI in culture and arts -  Human-AI interaction (tech crash course)
{: .no_toc}


## 📰 Announcements
{: .no_toc }

10.02.2026 - Save the date! The tech crash course on AI in Culture and Arts is coming soon. First bloc will be on **Wednesday, April 22nd** and **Thursday, April 23rd, 2026** at the **MUC.DAI**.

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
## What is AICA? 

The Digitization College "Artificial Intelligence in Culture and Arts" (AICA) aims to equip students at the [University of Music and Performing Arts Munich](https://hmtm.de/) (HMTM) and [Hochschule München University of Applied Sciences](https://www.hm.edu/en/index.en.html) (HM) with necessary skills to impact AI innovations in the creative and cultural industries.

[Learn more about AICA](https://www.wavelab.io/aica/){: .btn .btn-green
 target="_blank"}


## What is the crash course on Human-AI interaction ?

Artificial intelligence (AI) is increasingly impacting the cultural and creative sectors. In particular, machine learning algorithms can now generate unprecedented synthetic media, transforming how we create, produce, and distribute art and culture. Students must develop a theoretical and practical understanding of machine learning to comprehend such transformative technology and foster the development of meaningful human-AI interactions.
This course addresses this need and delves into interactive machine learning for the cultural and creative sectors. The course is intended for art, cultural management, design, and computer science students. After this course, students will master the theoretical and technological foundations of machine learning, be able to train and (critically) evaluate machine learning models, and deploy them in meaningful interactive systems.
The course is structured in three 2-day blocks (6 days in total). Each block provides theoretical lectures and hands-on activities to develop interactive machine-learning systems for image, sound, and text-based applications in the creative and cultural sectors. Every teaching day starts with a lecture and discussion in the morning, followed by a hands-on session on the same topic in the afternoon.

The AICA tech crash course will be hosted at the Wavelab, in the Summer Semester, **starting April 2026**.


## Learning outcomes

After successful participation in this course, students are able to:

- Understand the basics of information theory, logical and probabilistic thinking and computation. 
- Understand the history and current state of AI: students will be able to explain the different waves of AI (symbolic, connectionist), precisely identify machine learning algorithms, and explain their distinctive characteristics (dataset, optimization, loss, etc.).
- Trainand (critically) evaluate machinelearning algorithm: students will be able to explain and apply the main steps of the development cycle of machine learning, from data collection, analysis, preprocessing, training, and evaluation. They will be able to critically examine a learning curve and performance metrics to assess the performance of their machine-learning models. Furthermore, they will be able to critically discuss the limitations of their model from the content of their dataset and from the perspective of bias and fairness.
- Create interactive machine learning systems: students can design and implement interactive machine learning systems for image, sound, and text-based applications in the creative and cultural sectors. Three examples of interactive systems will be showcased in this course: a teachable image classifier, a gesture-to-sound synthesizer, and a tool for semantic and multi- modal exploration of museum archives. Students already familiar with programming and ma- chine learning will be able to dive deeper into the design and development of novel interactions with machine learning algorithms.

## Prerequisites

The module is designed as an interdisciplinary venue that brings together a range of perspective.
It is aimed at all students enrolled in a third-year Bachelor's program at Hochschule München University of Applied Sciences (HM) or the Hochschule für Musik und Theater München (HMTM). Students in Master's programs are also welcome. Students with prior computer science and machine learning knowledge will be assigned dedicated and more advanced activities to develop interactive ML systems using the open source [Marcelle toolkit](https://marcelle.dev/).

To apply, please refer to the [Subscription section]({% link content/subscription.md %}).

## Course content

Structured over three 2-day blocks (6 days in total), the course addresses:

1. **Introduction (Block 1, Days 1 & 2)**: This introductory block focuses on the history and principles of artificial intelligence from a computer science perspective. You will encounter core concepts such as *supervised learning*, *regression*, *classification*, and the full machine learning development cycle — from data collection and annotation to training, evaluation, and deployment. You begin by training a small neural network directly in the browser (via a [p5.js sketch](https://editor.p5js.org/BZoennchen/sketches/mHhBWnuoI)) to map spatial positions to musical notes. You then train your first image classifier using Google's [Teachable Machine](https://teachablemachine.withgoogle.com/) and [Marcelle](https://marcelle.dev/), and critically examine its performance using *confusion matrices*, *learning curves*, and discussions of *bias and fairness*. The block closes with a hands-on challenge — controlling a game of Snake with your body via a camera-based classifier — and a deeper dive into regression and classification using Python and Jupyter notebooks on [Google Colab](https://colab.research.google.com/).

2. **From Neural Networks to Generative Models (Block 2, Days 3 & 4)**: This block bridges the interactive experiments of Block 1 with the Python code running underneath them, then moves from classification into *generation*. Day 3 starts by re-implementing the browser sketch in PyTorch, introduces the *perceptron* and its famous limitations, and then covers *autoencoders* — your first generative model, capable of compressing data into a *latent space* and reconstructing new examples from it. The second half of the day turns to music: you represent symbolic music in Python using `music21`, compose short pieces via algorithmic rules, and build a *Markov chain* that imitates the style of Bach. Day 4 scales this up with neural sequence models: you encode melodies as data, then train a *feed-forward network*, an *LSTM*, and a *Transformer* — each progressively more powerful — to generate music autoregressively. The concept of *temperature* is introduced as a way to control the creativity of the generated output.

3. **Using Large Models (Block 3, Days 5 & 6)**: In the final block, you shift from training models from scratch to working with *large pre-trained models*. You load a pre-trained sentence-transformer, inspect its *embedding space*, and use *cosine similarity* to measure semantic relatedness between musical and textual concepts. You then explore four *decoding strategies* — greedy decoding, temperature sampling, top-k, and top-p (nucleus) sampling — to understand how sampling choices shape the character of generated output. The block closes with two approaches to adapting a pre-trained model to a new style without retraining from scratch: *transfer learning* (freezing most layers and updating only the last few) and *LoRA* (Low-Rank Adaptation), a parameter-efficient method that adds small trainable adapter matrices while keeping the original weights frozen. A bonus section applies LoRA to GPT-2 fine-tuned on Shakespeare.

## Tutorials and teaching methods

This website provides a range of tutorials and ressources, organized by topic and in increasing order of difficulty.

[Tutorial overview]({% link content/tutorials/tutorials.md %}){: .btn .btn-green
 target="_blank"}

A typical day of teaching starts with a lecture on a topic, followed by a hands-on session where students can apply the concepts learned in the lecture. The hands-on sessions are based on the tutorials provided on this website.

## Evaluation and ECTS

You will earn **2 ECTS** for the validation of the course.

The evaluation will be based on:
- **Attendance**: TBA
- **Completion of in-class practical work**: 
    - HM students must ... TBA 
    - HMTM students must ... TBA
    - All students must ... TBA

If you do not finish during the in-class sessions, you will have to finish it at home. Tutorials and your homework / assignments must be uploaded before the end of **10th of July** [here](https://syncandshare.lrz.de/preparefilelink?folderID=2Jmzaj6Sx24nh96gohfFN). The **password** will be provided in the course.

<!-- ## Credits and attributions

The tutorial are based on several **open-source tools and libraries** developed by talented researchers and developers. Without them, this course would not be possible. 
Discover all of them in section [Credits and attributions](/docs/credits){: target="_blank"}. -->

## License

The new teaching material (tutorials and code) created for the course is available under the [Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).
**Each tool and library demonstrated in the tutorials is subject to its own license.**
