---
layout: default
title: 5 & 6. Using large models
nav_order: 5
parent: Tutorials
---

# Day 5 & 6 - Using large models
{: .no_toc}

On days five and six you shift from training models from scratch to working with **large pre-trained models**. You will learn how neural networks represent meaning as vectors, how to steer their output through decoding choices, and how to adapt them to new tasks without retraining billions of parameters.

{: .note-title }
> Note
>
> The central question across both days is: *how can we make a model that already knows a lot do something slightly different?* This question — and the family of techniques that answer it — underpins almost everything happening in applied AI today. As you move through the notebooks, ask yourself: what is frozen, what is changed, and why?

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## R) Pre-trained models and embeddings

Modern AI models are not trained from scratch for every application. They are **pre-trained** on massive datasets and then shared for others to reuse. A key side-effect of this training is that the model learns to represent concepts as **embedding vectors**: numerical coordinates in a high-dimensional space where semantically similar items end up close together.

In the following notebook you will load a pre-trained sentence-transformer, inspect its embedding space, visualise how musical and textual concepts cluster, and use cosine similarity to measure semantic relatedness.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A3_using_large_models/10_1_pretrained_models_and_embeddings.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## S) Decoding strategies

A language model does not generate text directly. At each step it produces a **probability distribution** over all possible next tokens. How you sample from that distribution determines everything: the coherence, creativity, and diversity of the output.

This notebook compares four strategies: **greedy decoding** (always pick the most likely token), **temperature sampling** (scale the distribution before sampling), **top-k sampling** (restrict to the *k* most likely tokens), and **top-p (nucleus) sampling** (restrict to the smallest set of tokens whose cumulative probability reaches *p*). You will see how each strategy changes the character of the generated output.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A3_using_large_models/10_2_decoding_strategies.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## T) Transfer learning

The folk-song transformer trained in block 2 learned the style of German folk music. **Transfer learning** asks: can we adapt it to a completely different style, e.g. Bach chorales, without starting from scratch?

The answer is sometimes yes: by **freezing** most of the network's weights and only updating the last few layers, we preserve the general musical knowledge while nudging the output towards the new style. This notebook walks through the freeze-and-fine-tune procedure and lets you listen to the result.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A3_using_large_models/10_3_transfer_learning.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## U) LoRA — parameter-efficient fine-tuning

Freezing layers is practical but coarse: you choose entire layers to update or leave frozen. **LoRA** (Low-Rank Adaptation) is more surgical. Instead of selecting which layers to touch, it adds tiny trainable **adapter matrices** alongside every targeted weight while keeping the original weights permanently frozen. For large models this can reduce the number of trainable parameters to less than 1% while still achieving a clear style shift.

You will implement a `LoRALinear` module from scratch, inject adapters into the folk-song transformer, and compare the result with the partial-freeze approach from section T. A bonus section demonstrates LoRA at real scale: GPT-2 (124 million parameters) fine-tuned on Shakespeare's plays, where the style shift from modern English to Elizabethan prose is immediately readable.

<a href="https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A3_using_large_models/10_4_lora.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## V) Reflection — from scratch to adaptation

You have now seen a complete arc of model development across all three blocks:

1. **Training from scratch** — folk-song transformer trained on German folk songs (block 2)
2. **Transfer learning** — freezing most layers, updating only the last block (section T)
3. **LoRA** — parameter-efficient adapters spread across all layers (section U)
4. **Large pre-trained models** — reusing embeddings and controlling output (sections R & S)

As a group, discuss the following questions:

- When would you choose full fine-tuning over LoRA? What are the trade-offs in terms of compute, data size, and risk of forgetting?
- The decoding strategy (section S) has a large effect on the feel of the output. Which strategy seemed most useful for creative work, and why?
- LoRA's key insight is that the *change* needed to adapt a model is low-rank
— it lives in a much smaller subspace than the full weight matrix. Can you think of an analogy from music or art: a small, targeted modification that produces a large stylistic shift?