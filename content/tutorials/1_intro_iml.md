---
layout: default
title: 1. Introduction to interactive machine learning
nav_order: 1
parent : Tutorials
---

# Day 1 - Introduction to interactive machine learning
{: .no_toc}

<image src="https://live.staticflickr.com/1571/25139082514_36dcf31ae0_b.jpg" style="width: 700px; display: block; margin-left: auto; margin-right: auto;"/>
<figcaption>In addition to learning the basics of programming and machine learning, you'll also have to predict the number of visitors to Bristol's museums based on the weather forecast.</figcaption>


{: .note-title }
> Note
>
> The first day of the course aims to partly homogenize levels and teach foundational concepts in data science and machine learning (ML) through hands-on turorials.
> We recommend all attendants to carefully follow its content. If the content is too easy for you, please tell your scientific instructors and they will provide you with additional resources. Inversely, if the content is too hard for you, please tell your scientific instructors and they will provide you with additional explanations.

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## A) Brief : Module introduction

Please find the slides of the module description and the schedule of the course below:

[Slides : Module introduction](https://github.com/aica-wavelab/aica-assignments/blob/main/A1_introduction/module_introduction.pdf){: .btn .btn-green
 target="_blank"}

## B) Lecture : Introduction to artificial intelligence

Please find the slides of the lecture on the introduction to AI and machine learning below (we will probably revisit these slides from time to time):

 [Slides : Introduction to Deep Learning](https://github.com/aica-wavelab/aica-assignments/blob/main/A1_introduction/ai_ml_introduction_deep_dives.pdf){: .btn .btn-green
 target="_blank"}

## C) Hands-on : train your first model (classification and regression)

First go to [classification sketch](https://editor.p5js.org/BZoennchen/sketches/mHhBWnuoI).

You are looking at a blank canvas. By clicking on it, you will teach a small neural network to associate **locations in space** with **musical notes**. Once trained, the network will listen to your clicks and predict which note belongs at that spot — and play it.

This is supervised learning in its most direct form: you provide the examples, the network generalises from them.

### Step 1 - Start the program

Click on the play button.

### Step 2 — Collect training data

Your first job is to be the teacher.

1. **Choose a note** by holding down one of the letter keys on your keyboard: `A`, `B`, `C`, `D`, `E`, `F`, or `G`.
2. **Click somewhere on the canvas.** A circle appears at that spot labelled with your chosen note, and you hear the note play.
3. **Repeat** — build up a collection of points across the canvas, one region per note.

> **Tip:** Think of dividing the canvas into territories. Maybe `C` lives in the top-left, `G` in the bottom-right, and so on. You don't have to be tidy about it — messy, overlapping regions make the exercise more interesting.

You can use as many or as few notes as you like, but **at least 3 notes with roughly 5–10 points each** gives the network something meaningful to learn.

### Step 3 — Train the network

Once you have collected enough data, press **`T`** to start training.

The network will run for **200 epochs** — 200 passes through your training data, adjusting its internal weights a little each time to reduce the number of mistakes. You can follow the progress in the browser. A popup window will appear.

When training is finished, the canvas label changes from *collecting* to *predicting*.

### Step 4 — Test your model

Now you are no longer the teacher — you are the examiner.

**Click anywhere on the canvas.** The network predicts which note belongs at that location (shown as a blue circle) and plays it.

Ask yourself:
- Does the prediction match what you intended when you placed your training points?
- Where does the network get it right? Where does it make mistakes?
- What does it do in areas where you placed **no training data at all**?

### Step 5 - Iterate

Press **`R`** to go back to collecting mode. Your training data is still there but but your network resets — now you can add more training points and retrain.

Try these experiments:

**Experiment 1 — More data, cleaner regions**
Place 20+ points per note in clearly separated areas. Does accuracy improve?

**Experiment 2 — Intentional overlap**
Place two different notes in almost the same location. What does the network do? What does this tell you about classification boundaries?

**Experiment 3 — Sparse data**
Train with only 2–3 points per note. Where does the network feel confident? Where does it hesitate (listen to the predictions in border zones)?

**Experiment 4 — Non-obvious patterns**
Try placing one note in two completely separate corners of the canvas, with other notes in between. Can the network learn a non-contiguous region?

### What is the network actually doing?

Under the hood, this sketch uses a small neural network (via **ml5.js**) with:

- **2 inputs:** the `x` and `y` coordinates of your click
- **Hidden layers** that learn weighted combinations of those inputs
- **7 possible outputs:** one probability per note — the network picks the highest

During training, it is finding a way to divide the 2D canvas into regions — a **decision boundary** — that best fits your examples. With only 2 inputs, you can almost imagine this geometrically: the network is drawing curved lines through the canvas to separate one note's territory from another's.

### Step 6 - Regression

Now go to [regression sketch](https://editor.p5js.org/BZoennchen/sketches/lHQAFZhCi).

Repeat *Step 1* to *Step 5* what do you observer?

## D) Hands-on : train your first image classifier with Marcelle

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
On the right, you can see the global accuracy and a confusion matrix computed on the test set only. The test accuracy is a better indicator of the model performance. If the test accuracy is much lower than the training accuracy, it means that the model is overfitting the training set and that it will not generalize well to new data.

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


#### Using your own machine

If you are advanced and you want to run the code on your machine you can clone the Git repo. Launch the following command:
    
    git clone https://github.com/aica-wavelab/aica-assignments.git

If you struggle with terminal commands, you can also download the repository as a zip file by clicking on the green button `Code` on the top right of the github repository page, then `Download ZIP`.

Now open the folder `A1_introduction` and launch the jupyter notebook server by typing the following command in the terminal:

    jupyter notebook

Then click on the first file `1_tutorial_jupyter_notebook.ipynb` to open the tutorial and follow the instructions.

Alternatively, you can launch the Anaconda navigator (desktop application) and open the jupyter notebook application from there. Then, navigate to the folder `A1_introduction` and open the first file `1_tutorial_jupyter_notebook.ipynb`.