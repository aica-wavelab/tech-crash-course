---
layout: default
title: 3. From neural networks to generative models
nav_order: 3
parent : Tutorials
---

# Day 3 - From neural networks to generative models
{: .no_toc}

The third day bridges what you learned in Block 1 — training classifiers and regression models interactively — with a deeper understanding of how neural networks work and how they can be used to **generate** new content, not just predict labels.

For both days of the second bloc you have to fill out an *reflection log* you find here:

[Docx : Reflection Log Template (Block 2)](https://github.com/aica-wavelab/aica-assignments/blob/main/A2_generation/Reflection-Log-Block2.docx){: .btn .btn-green target="_blank"}

You are encouraged to work in mixed teams! 

You can download the lecture slides here

[Slides : Algorithmic Composition using Neural Networks](https://github.com/aica-wavelab/aica-assignments/blob/main/A1_generation/melodygeneration_aica.pdf){: .btn .btn-green
 target="_blank"}

<!--

Furthermore, there is homework to do:

[Docx : Homework for HM students](https://github.com/aica-wavelab/aica-assignments/blob/main/A2_generation/Homework-Block2-HM-Students.docx){: .btn .btn-green target="_blank"}

[Docx : Homework for HMTM students](https://github.com/aica-wavelab/aica-assignments/blob/main/A2_generation/Homework-Block2-HMTM-Students.docx){: .btn .btn-green target="_blank"}

HMTM students can also do the homework of HM students if they prefer it!

-->

{: .note-title }
> Note
>
> The third day connects the interactive experiments from Block 1 to the Python code that runs underneath them, then introduces two foundational ideas in deep learning — the perceptron and the autoencoder — before moving into the music domain. Take the time to discuss with your group: you don't have to understand every line of code, but you should be able to explain what each notebook is *trying to do*.

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## H) From canvas to code — revisiting classification and regression

In Block 1 you trained a neural network by clicking on a canvas. Now you will see the exact same task expressed in Python.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/6_predicting_notes.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

This notebook trains a small PyTorch network to predict musical notes from `x`/`y` coordinates — the same inputs your browser sketch used. It covers both a **classification** version (pick one of seven notes) and a **regression** version (predict a frequency in Hz).

Work through the notebook in your group. Focus on recognising the pipeline you already know: data → model definition → training loop → evaluation. The code makes explicit what ml5.js was doing for you automatically.


---

## I) The perceptron — where it all started

Before multi-layer networks, there was a single neuron. This notebook tells the story of the **perceptron**: what it can do, what it famously cannot do, and why that limitation led directly to the deep networks you have been using.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/7_perceptron.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Pay close attention to the **XOR problem**: a simple logical function that a single neuron cannot learn, no matter how long you train it. This is not a limitation of the data — it is a geometric fact. Understanding it will help you appreciate why adding more layers is not just a trick, but a necessity.


---

## J) Autoencoders — learning to compress and generate

So far, every network you have used has been a *discriminative* model: given an input, predict a label or a number. An **autoencoder** is different — it learns to compress an input into a compact representation (the **latent space**) and then reconstruct it. This is your first encounter with a *generative* model.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/8_autoencoder.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

The notebook trains an autoencoder on the MNIST handwritten digit dataset. After training, you can explore the latent space: points nearby in that space correspond to images that look similar. You can also **interpolate** — pick two points in the latent space and move smoothly between them to generate new images that blend the two originals.

---

## K) Working with symbolic music in Python

From now on the subject is **music**. Before we can teach a network to generate music, we need to be able to represent music in Python. This section covers two notebooks that you can work through together.

### K.1 — music21 basics

The `music21` library lets you create, manipulate, and listen to symbolic music: individual notes, chords, rhythms, full scores.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_1_working_with_music21.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Work through the notebook to learn how to create `Note` and `Chord` objects, assemble them into a `Stream`, and export to MIDI. You do not need to memorise the API — focus on understanding what each building block represents musically.

### K.2 — Algorithmic composition

With `music21` in hand, you can compose music using pure rules and randomness — no machine learning involved yet.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_2_genuine_composing.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

This notebook explores how to use probability distributions, consonance/dissonance rules, and structured randomness to generate short musical passages.

---

## L) Style imitation with Markov chains

The day closes with your first statistical model of musical style. A **Markov chain** learns which notes tend to follow which other notes in a corpus — in this case, the music of Johann Sebastian Bach. It then generates new melodies by following those learned probabilities.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_3_style_imitation.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

This model requires no gradient descent. The "training" is simply counting: how often does note B follow note A in Bach's scores? The result is a transition matrix — a table of probabilities.


{: .note-title }
> Closing reflection for Day 3
>
> You have now seen three very different approaches to music generation: pure randomness and rules (K.2), statistical counting (L), and — coming tomorrow — neural networks. Before Day 4, think about: what would it take to generate music that genuinely sounds like a specific composer? Which of the approaches today gets closest, and why does it fall short?

---

## Submission

Submit your work, i.e. your reflection log, [here](https://syncandshare.lrz.de/preparefilelink?folderID=2Jmzaj6Sx24nh96gohfFN).
