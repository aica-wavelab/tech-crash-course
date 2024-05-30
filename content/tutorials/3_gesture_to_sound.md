---
layout: default
title: 3. Mapping gestures to sounds from demonstrations
nav_order: 3
parent : Tutorials
---

# Day 3 - Mapping gestures to sounds from demonstrations
{: .no_toc}

<image src="https://live.staticflickr.com/4365/37161246275_7cfcb13035_b.jpg" style="width: 700px; display: block; margin-left: auto; margin-right: auto;"/>
<figcaption>Photography from Corpus Nil from the artist Marco Donnarumma (IT/DE). The artist is using muscle contraction sensors to generate sounds. Link to the video: <a href="https://vimeo.com/152710490" target="_blank">Corpus Nil</a></figcaption>

---

## Table of contents
{: .no_toc .text-delta }

2. TOC
{:toc}

---


## Introduction

The third day of this class will show you:
- A novel application of machine learning in culture and art: **mapping gestures to sounds from demonstrations**.
- A novel graphical programming environment to develop interactive prototypes: **PureData**

Your goal will be to train a machine learning model to generate sounds from gestures. The training data will be collected by you, on spot, using the sensors from your smartphone. 

Please download the code and data from the [github repository](https://github.com/aica-wavelab/aica-assignments) and follow the instructions in the `A3_gesture_to_sound_mapping`.

[Github repository of the course](https://github.com/aica-wavelab/aica-assignments){: .btn .btn-green
 target="_blank"}

## Content of the repository

The repository contains the following folders:

- `puredata_cheatsheet.pd`: A patch with the main objects seen during the course and their keyboard shortcuts.
- `dub_siren_box`: A practical and fun exercise to start apply the concepts seen before. The patch reimplement this [hardware](https://www.youtube.com/watch?v=sCNiYJlU0DA).
- `mapping_by_demonstration`: Demonstration of how to map gestures to sound using the ml-lib library.

## Assigment

Implement a musical instrument using Plugdata and ml-lib. The instrument can map any signal to any sound or sound effect you'd like. You are then assigned to upload the files along with a short video of your instrument in action !

## Installation required

### Plugdata

Plugdata is a free/open-source visual programming environment based on pure-data. It is available for a wide range of operating systems. 
Please install plugdata for your operating system from the [plugdata website](https://plugdata.org/download.html).

### ml-lib

ml-lib is a library of machine learning externals for Max and Pure Data designed and developed by [Ali Momeni](http://alimomeni.net) and [Jamie Bullock](http://jamiebullock.com).

The goal of ml-lib is to provide a simple, consistent interface to a wide range of machine learning techniques in Max and Pure Data. The canonical NIME 2015 paper on ml-lib can be found [here](https://nime2015.lsu.edu/proceedings/201/0201-paper.pdf).

Full class documentation can be found [here](http://irllabs.github.io/ml-lib/).

Please download the latest release of ml-lib for your operating system from the [ml-lib website](https://github.com/irllabs/ml-lib/releases/).
Then copy the files into the PureData folder.

- On Windows, you can copy the files into the folder `C:\Program Files\plugdata\Extra\ml.lib`
- On MacOS, you can copy the files into the folder `Documents/plugdata/Extra/ml.lib`

### Streaming data from your phone

To stream sensors' data from your phone via the protocol OSC to your computer, you can use the following open-source applications:

- On Android: [Sensors2OSC](https://sensors2.org/osc/) can be installed via F-Droid
- On iPhone: [Data OSC](https://apps.apple.com/de/app/data-osc/id6447833736?platform=iphone) can be installed via the App Store

{: .warning}
> Both applications are free, open-source, and developed by independent developers. For this reason, it is possible that they trigger security alerts on your phone.




