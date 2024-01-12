---
layout: default
title: 3. Audio modelling and synthesis with neural networks
permalink: /docs/3_audio_modelling
nav_order: 6
---

# Audio modelling and synthesis with neural networks
{: .no_toc}

Neural networks prove to be a powerful tool to model and synthesize audio signals in the waveform domain.
This chapter will teach you how to train and use a real-time neural synthesizer using the [Real-Time Audio Variational autoEncoder (RAVE)](https://github.com/acids-ircam/RAVE) model developed by the [ACIDS team at Ircam](https://acids.ircam.fr/), and include it in your Pure Data patch with [nn~](https://acids-ircam.github.io/nn_tilde/).

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Audio modelling and synthesis with pre-trained neural networks

Recent advances in deep learning have enabled the development of neural networks that can model and synthesize audio signals in the waveform domain. After training on corpus of sound, the trained model can be used to generate new audio signals, or to transform existing ones.

In particular, the RAVE model is a variational autoencoder for fast and high-quality neural audio synthesis developed by Antoine Caillon and Philippe Esling from the ACIDS team in IRCAM. 

Trained RAVE models can be loaded in Pure Data or Max/MSP (paying alternative to Pd) using the `nn~` external. Let's have a look to their demonstration.

<iframe width="100%" height="420" src="https://www.youtube.com/embed/dMZs04TzxUI" title="Realtime Neural Audio Synthesis - RAVE + nn~ #1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

You can learn more about the specificity of the RAVE architecture on the tutorial below:

<iframe width="100%" height="420" src="https://www.youtube.com/embed/o09BSf9zP-0" title="IRCAM Tutorials / Rave and nn~" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

You can learn more about the RAVE model on the [official github repository](https://github.com/acids-ircam/RAVE).
Please find a demo of audio transfer in Pure Data using [`nn~`](https://acids-ircam.github.io/nn_tilde/) and a pre-trained model in the link below:

[Audio style transfer in Pd](https://github.com/aica-wavelab/aica-project-workshop/tree/main/3_neural_synthesis){: .btn target="_blank"}

Other pre-trained models are available on [here](https://acids-ircam.github.io/rave_models_download) and [here](https://iil.is/news/ravemodels).

## Train your model from your own corpus of sound

Training a RAVE model on your own corpus of sound is possible but computationally expensive. We cannot provide you with a GPU (Graphical Processing Unit), used to train artificial neural network. However, you can use the following Google Colab written by [hexorcismos](https://github.com/moiseshorta), which is a computational notebook that runs on GPU hosted by Google:

[Training a RAVE model on Google Colab](https://colab.research.google.com/drive/1ih-gv1iHEZNuGhHPvCHrleLNXvooQMvI?usp=sharing){: .btn target="_blank"}

