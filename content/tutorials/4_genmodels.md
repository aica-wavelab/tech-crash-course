---
layout: default
title: 4. Sequence models and generative music
nav_order: 4
parent : Tutorials
---

# Day 4 - Sequence models and generative music
{: .no_toc}

On the fourth day you move from statistical models to neural networks trained end-to-end on music. You will learn how to represent melodies as data, then train three progressively more powerful models — a **feed-forward network**, an **LSTM**, and a **Transformer** — each generating music in a different way. The day closes with a listening session comparing all three.

For both days of the second bloc you have to fill out an *reflection log* you find here:

[Docx : Reflection Log Template (Block 2)](https://github.com/aica-wavelab/aica-assignments/blob/main/A2_generation/Reflection-Log-Block2.docx){: .btn .btn-green target="_blank"}

You are encouraged to work in mixed teams! 

You can download the lecture slides here:

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
> Today you will encounter three different neural architectures applied to the same creative problem: generating a melody. As you work through each notebook, keep asking the same question — *what can this model do that the previous one could not?* The answer will help you understand why the field moved from simple networks to recurrent networks to transformers.

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## M) Representing music for machine learning

Before any neural network can learn from music, the music has to become numbers. This section covers two notebooks that introduce the two most common ways to do this.

### M.1 — One-hot encoding

Categorical data — like a note name ("C", "D#", "G") — cannot be fed directly into a neural network as a single integer. **One-hot encoding** turns each category into a binary vector: all zeros except for a single `1` in the position corresponding to that category.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_4_one_hot_encoding.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

### M.2 — Melody representations

There are several ways to represent a melody as a sequence of numbers. This notebook introduces the **piano roll** (a 2D binary matrix of pitch vs. time) and a **note-based DataFrame** (a table of note events with pitch, onset, and duration), as well as a compact 1D piano roll encoding.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_5_melody_representations.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## N) Learning the Markov matrix with a neural network

Yesterday you computed a Markov transition matrix by counting note transitions in Bach's music. Today you will let a **feed-forward network** (FFN) learn the same matrix through gradient descent — without explicitly counting anything.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_6_ml_ffn_markov.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

The network takes a one-hot-encoded note as input and predicts the probability distribution over the next note. This is conceptually identical to the Markov chain — but now it is learned, not hand-computed.

---

## O) LSTM — generating melodies with recurrent networks

A feed-forward network has no memory: each prediction depends only on the current input. A **Long Short-Term Memory** (LSTM) network is designed to remember information across many steps of a sequence — making it much better suited to music, where the "right" next note often depends on what happened several notes ago.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_7_ml_rnn.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

After training, the network generates melodies autoregressively: it predicts the next note, feeds that prediction back as the next input, and repeats. A **temperature** parameter controls how creative (or chaotic) the predictions are — low temperature produces safer, more predictable melodies; high temperature introduces more variety but also more randomness.

---

## P) Transformer — attention-based melody generation

The **Transformer** is the architecture behind modern large language models (GPT, Claude, Gemini). Applied to music, it works in a similar way: given a sequence of past notes, predict what comes next. Unlike the LSTM, it does not process the sequence step by step — instead, it uses **self-attention** to look at all previous notes simultaneously and decide which ones are most relevant for the current prediction.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_generation/9_8_ml_transformer.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

The notebook implements a **decoder-only Transformer** with **causal masking** — each position can only attend to positions before it, which ensures the model cannot "cheat" during training by looking ahead at the answer.

---

## Q) Reflection — comparing the models

You have now seen five approaches to generating music across the last two days:

1. Pure rules and randomness (section K.2)
2. Markov chains — statistical counting (section L)
3. Feed-forward network — learned Markov matrix (section N)
4. LSTM — sequence memory (section O)
5. Transformer — global attention (section P)

As a group, generate a short melody (8–16 notes) using the same seed material in each of the last three models. Listen to the results and discuss:

---

## Submission

Submit your work, i.e. your reflection log, [here](https://syncandshare.lrz.de/preparefilelink?folderID=2Jmzaj6Sx24nh96gohfFN).