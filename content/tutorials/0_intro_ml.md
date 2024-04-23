---
layout: default
title: 0. Introduction to data science and machine learning
nav_order: 4
parent : Tutorials
---

# Day 0 - Introduction to data science and machine learning
{: .no_toc}

{: .note-title }
> Note
>
> The first day of the course aims to homogenize levels and teach foundational concepts in data science and machine learning (ML) through hands-on turorials.
> We recommend all attendants to carefully follow its content. If the content is too easy for you, please tell your scientific instructors and they will provide you with additional resources. Inversely, if the content is too hard for you, please tell your scientific instructors and they will provide you with additional explanations.

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---



## A) Brief : Module introduction

Please find the slides of the module description and the schedule of the course below:

[Slides : Module introduction](/slides/0_module_introduction.pdf){: .btn .btn-green
 target="_blank"}

## B) Lecture : Introduction to AI and machine learning

Please find the slides of the lecture on the introduction to AI and machine learning below:

[Slides : Introduction to AI and machine learning](/slides/0_introduction_to_ai_and_machine_learning.pdf){: .btn .btn-green
 target="_blank"}

## C) Hands-on : train your first image classifier with Marcelle

Let's practice !

[Go to the Marcelle app!](https://aica-wavelab.github.io/tech-crash-course/content/demos/image_classification){: .btn .btn-green
 target="_blank"}

You can find the source files of this activity in the folder `train_your_first_classifier` of the github repository of the course.

### Data collection

The first step of the development cycle of ML is data collection. It consists in collecting and annotating data samples that can be used by an ML algorithm to learn a mapping from inputs to outputs. In the previous example, the data samples are images collected with your webcam and the corresponding labels you provided.
If pairs of input and output are provided in the training set, we talk about **supervised learning**. If only inputs are provided, we talk about **unsupervised learning**.

The data samples are usually gathered in two sets: the **training set** and the **test set**. The training set is used to train the ML model, while the test set is used to evaluate the performance of the trained model. In other words, the training set is the exemples you work on during the semester, while the test set is the final exam.

We provide various miniature image datasets that represent classification problems in engineering, medecine, and public health:

- miniMASK: a dataset of 3 classes of images (with masks, without masks, and with masks incorrectly worn);
- miniROAD: a dataset of 3 classes or green, orange, and red traffic lights;
- miniTRASH: a dataset of 3 classes of images (packaging, transparent glass, and opaque glass);
- miniRETINA: a medical dataset of 3 classes of retinoscopic images (healthy, macular degeneration, and diabetic retinopathy);
- miniSKIN: a medical dataset of 2 classes of dermatoscopic images (benign and malignant skin lesions);

On the [`Data collection`](https://aica-wavelab.github.io/tech-crash-course/content/demos/image_classification/#) page, click on one button to select the dataset you want to work with for the rest of the tutorial.

{: .note-title }
> Hints
>
> Take the time observe each images (by clicking on the thumbnails). Are the differences between each classes obvious to you?



### Training

The training phase comprises three steps: 

C.1. **Features selection** : in our case, we will use a pre-trained neural network called MobileNet that extract 1024 features from images. These features were learned from a large dataset of images (ImageNet) and can be used to represent any image.

C.2. **Model selection** : Many machine learning models exist and were developed. In our case, we will use a model called multi-layer perceptron (MLP). It is a simple artificial neural network composed of an input layer (in our case, the 1024 features from MobileNe, some hidden layers that we can choose, and an output layer (the number of classes).
Two other parameters are important to set. The **batchSize** and the number of **epochs**. An artificial neural network can updates its neurons using several examples at the same time. The batch size indicates the number of images that will be used at each round to update the neurons. The number of epochs indicates the number of times the whole training set will be used to update the neurons. The higher the number of epochs, the more the model will be trained. However, if the number of epochs is too high, the model might overfit the training set and will not be able to generalize to new data. You can choose the number of hidden layers and neurons per layer, the batch size, and the number of epochs on the [`Training`](hhttps://aica-wavelab.github.io/tech-crash-course/content/demos/image_classification/#training) page of the application. 


C.3. **Training** : Click on the training button to start the neural network optimization.
You will then see two different learning curves appearing. The represent the losses and accuracies as a function of the number of epochs. The loss is a measure of the error between the predictions of the model and the true labels. The accuracy is the percentage of correct predictions. 
A validation loss and accuracy are computed using a portion of the training set that is not used for the training. 
If the validation loss and validation accuracy are not improving, it means that the model is overfitting the training set and that it will not generalize well to new data. In this case, you should stop the training and reflect on the parameters of the model or the data used for the task.

### Testing

At this point, the model only saw the training set, eventhough it artificially splited this set into a training and validation set. To really assess the model performance, we need to compute a test accuracy on unseen images. On the [`Testing`](https://aica-wavelab.github.io/tech-crash-course/content/demos/image_classification/#testing) page of the application, you can see two **confusion matrices**. On the left is shown the global accuracy and a confusion matrix computed on the training set only. The rows of the confusion matrix represent the true labels (what should be predicted), while the columns represent the predicted labels. The diagonal of the matrix represents the number of correct predictions. A confusion matrix gives a finer view of which class is confused with which class. 
On the left, you can see the global accuracy and a confusion matrix computed on the test set only. The test accuracy is a better indicator of the model performance. If the test accuracy is much lower than the training accuracy, it means that the model is overfitting the training set and that it will not generalize well to new data.

{: .note-title }

{: .note-title }
> Questions
>
> 1. For the task you selected, what averaged accuracy would you obtain with a random classifer? Is the trained classifier better than a random classifier in your case? 
> 2. What difference do you observe between the training and test accuracies? What does it mean?
> 3. Which classes are the most confused? Why do you think so? Among the confusions you identified, is there any would be more problematic than others in the problem selected? 
> 4. What would you do to improve the model performance?

### Deployment

Now you trained and test a machine learning model, you can learn more about its behavior by observing its predictions on particular images. On the [`Deployment`](https://aica-wavelab.github.io/tech-crash-course/content/demos/image_classification/#deployment) page of the application, you can see the predictions of the model when you click on the thumbnails of the training or test set.

Machine learning models can be noisy and biased. **Noisiness** indicates that the model is not stable and that it can give different predictions for similar inputs (it's unpredictably wrong). **Bias** indicates that the model is wrong or unfair for similar inputs (it's always wrong in the same way). 
Biases in ML models can lead to discrimination as illustrated in many different controversies over the past years. These incidents are documented on a public website called [AI incident database](https://incidentdatabase.ai/cite/37/).

{: .note-title }
> Questions
>
> Among erroneous predictions, can you identify biases? Are these biases explained by the training data? Are these biases problematic in the problem selected?

Now you know the elementary steps to train and test a machine learning model, you can try the same process on another dataset. The next section will teach you how to conduct the same steps using a programming langage (Python) and dedicated ML libraries.


## D) Tutorials in Python

### How to download and launch the tutorials ?

First go to the github repository of the course:

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments){: .btn .btn-green
 target="_blank"}

Then, download the repository on your computer.

In a terminal, launch the following command:
    
    git clone https://github.com/aica-wavelab/aica-assignments.git

If you struggle with terminal commands, you can also download the repository as a zip file by clicking on the green button `Code` on the top right of the github repository page, then `Download ZIP`.

Now open the folder `A0_introduction` and launch the jupyter notebook server by typing the following command in the terminal:

    jupyter notebook

Then click on the first file `01_tutorial_jupyter_notebook.ipynb` to open the tutorial and follow the instructions.

Alternatively, you can launch the Anaconda navigator (desktop application) and open the jupyter notebook application from there. Then, navigate to the folder `A0_introduction` and open the first file `01_tutorial_jupyter_notebook.ipynb`.

### What will you learn ?

For the first day, all tutorials are in Python and use jupyter notebooks.

This folder `A0_introduction` contains:
- A tutorial on [jupyter notebooks](https://jupyter.org/): `01_tutorial_jupyter_notebook.ipynb`
- A tutorial on the basics of the [Python programming language](https://www.python.org/): `02_tutorial_python.ipynb`
- A tutorial on data science basics using the [pandas library](https://pandas.pydata.org/) and [seaborn library](https://seaborn.pydata.org/): `03_tutorial_data_science.ipynb`. You will apply data sciences techniques to analyze the curation of the Museum of Modern Art (MoMA) in New York City, USA.
- A tutorial to train your first classifier in Python using the [keras library](https://keras.io/): `04_tutorial_machine_learning.ipynb`. You will apply machine learning techniques to predict the number of visitors in the museums of Bristol, UK.


## E) For advanced students: Create your own interactive ML web application

The interactive applications you used were programmed using Marcelle.
[Marcelle](https://marcelle.dev/) is a modular open source toolkit for programming interactive machine learning applications. Marcelle is built around components embedding computation and interaction that can be composed to form reactive machine learning pipelines and custom user interfaces. This architecture enables rapid prototyping and extension. Marcelle can be used to build interfaces to Python scripts, and it provides flexible data stores to facilitate collaboration between machine learning experts, designers and end users.

If you want to learn how to create your own interactive machine learning application, please read the [introduction](https://marcelle.dev/guide/) and follow the tutorial on the Marcelle website:

[Marcelle tutorial](https://marcelle.dev/guide/getting-started.html){: .btn .btn-green target="_blank"}

{: .note-title }
