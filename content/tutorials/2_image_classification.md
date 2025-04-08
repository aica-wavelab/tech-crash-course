---
layout: default
title: 2. Image classification of museum artefacts
nav_order: 2
parent : Tutorials
---

# Day 2 - Image classification of museum artefact
{: .no_toc}

<image src="https://production-media.paperswithcode.com/datasets/Screenshot_2021-02-01_at_15.22.19.png" style="width: 700px; display: block; margin-left: auto; margin-right: auto;"/>
<figcaption>Example of artefacts from the Museum Art Medium (MAMe) dataset you will be working on</a></figcaption>
---

## Table of contents
{: .no_toc .text-delta }

2. TOC
{:toc}

---


## Introduction

In our second day, you will be asked to train an image classifier to classify images of museum artefacts.

Your goal will be to recognize the artistic medium of the artefact in the image. 

Please download the code and data from the [github repository](https://github.com/aica-wavelab/aica-assignments) and follow the instructions in the `A1_image_classification_of_museum_artefacts`.

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments){: .btn .btn-green
 target="_blank"}

Alternatively, you can work in Google Colab.

[Google Colab](https://colab.research.google.com/github/aica-wavelab/aica-assignments/blob/main/A2_image_classification_of_museum_artefacts/assignment_classification_museum_artefact.ipynb){: .btn .btn-green
 target="_blank"}

## Dataset

To train your machine learning image classifier, you will use the [Museum Art Medium (MAMe) dataset](https://hpai.bsc.es/MAMe-dataset/), that contains high and low resolution images of artefacts from:

- The Metropolitan Museum of Art of New York
- The Los Angeles County Museum of Art
- The Cleveland Museum of Art


The dataset is available at [MAMe dataset](https://hpai.bsc.es/MAMe-dataset/) and includes:

- **Artefact images**: ~37,000 in both high and low resolution (224x224 pixels)
- **Metadata** (`MAMe_dataset.csv`): the museum provenance, the widht, height, product size, and aspect ratio.
- **The artistic medium** (`MAMe_labels.csv`): 29 categories of artistic medium (i.e. materials and techniques), such as "oil on canvas", "painting", "photograph", "ceramic", etc.

In addition, we provide the file `data/MAMe_dataset_extended.csv`, which is similar to `MAMe_dataset.csv` but we added an extra column that contains the MobileNetV1 features for each image. [MobileNetV1](https://paperswithcode.com/method/mobilenetv1) is a generalist and pre-trained neural network specialized to extract visual features. It has been trained on 1000 categories of images from the ImageNet dataset. 

<div class="alert alert-info">

**Assignment**: Your goal is to train the most accurate model to predict the medium of an museum artefact. Beside vision-related data, you are allowed to use the dimension of the object (width, height etc.) in your features. You must document all steps of the development cycle: data collection, data processing, feature selection, training, and evaluation.
</div>

- Figures are encouraged and should be commented and interpreted
- Every choice must be discussed and explained

