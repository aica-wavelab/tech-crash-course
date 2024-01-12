---
layout: page
title: Group feedback
nav_exclude: true
nav_order: 2
---

## Group A : Human-machine co-improvisation

### Progresses

- Implemented the second half of the pipeline: the factor oracle is now able to generate new notes from the sequence learned. These notes are played by a minimal synthesizer. You almost have a proof of concept of the system.

### Next steps for the PoC

1. Crash test the factorOracle: try to really co-impprovise with the machine. Does it stay locked in loops? What if you train with longer musical phrases? Please document your observations.

2. Improve the audio synthesis:  To improve your minimal synthesizer, learn about ADSR envelope and ways to implement it in PureData, learn about the timber quality of a saxophone and how to reimplement it. In addition, please have a look to audio style transfer using RAVE and nn~ on tutorial #3.


## Group B : Collaborative visual story-telling

### Progresses

- The group successfuly use the openAI API to generate prompts from story fragments and generate an image from the prompt (using DALL-E).
- The narrative of the project was discussed as it does not clearly match the cultural and creative industries but rather gamify the text-to-image recreative practice. We discussed to reframe the project as a tool for amateur storyboard creation.
- The implementation was assigned according to goup member's technical abilities. Moritz will learn about front-end development while Felix will tackle the back-end devlopment using the [Flask python framework](https://flask.palletsprojects.com/en/3.0.x/).


### Next steps for the PoC

- The narrative of the project is still unclear. Please interview potential users to understand how they would use and comprehend your project
- Design and sketch users' interactions (as a story board?)
- The proof of concept should be a working application where users enter a prompt and receive an image.


## Group C : Music generation from movements and dance

### Progresses

- The group should possess all necessary hardware (piezoelectric sensors, armband, Arduino, bread board etc.)
- The group successfuly assign roles for the project. Fabian is in charge of sound synthesis with SuperCollider. Matthias implemented the project's architecture and is in charge of the hardware. Marius is in charge of estimating bpm using recurrent neural network.
- The program architecture is clear and functionnal.
- The group succesfully applied a peak detection algorithm on fake data.

### Next steps for the PoC

- Stream the piezoelectric sensor data to the computer
- Try a simple LSTM (recurrent neural network) to estimate the bpm (or localization) from the piezoelectric sensor data
- Test the entire pipeline, from sensor to sound synthesis

## Group D : Virtual archives of clothing artefacts

### Progresses

- The group decided to focus an interactive "mirror" for visitors to try moving clothing artefacts. An alternative direction was to let users "look around" a still clothing artefacts by tracking people's head. This direction was discarded.
- The group did a technological watch of proprietary solutions for pose estimation from images. None of them are both free and in real-time.
- The group successfully used [BlendArMocap](https://github.com/cgtinker/BlendArMocap) in Blender to extract a skeleton from a video stream. The pose estimation is very slow.
- The group successfully infered a skeleton from a single frame using [Google's mediapipe](https://mediapipe-studio.webapps.google.com/studio/demo/pose_landmarker). It can potentially speed up the 

### Next steps for the PoC

- Model any clothing artefact and map skeleton joints to the clothing artefact.

## Group E : AI-augmented audio guide

### Progresses

- The group successfully called text-to-speech, speech-to-text and conversational bots from the OpenAI API.
- The work was divided between group members. Julian would focus on the back-end development with [Flask](https://flask.palletsprojects.com/en/3.0.x/). Philip will focus on the front-end development in HTML, CSS, and JS (audio recording and playback). Scientific tutors will help to conncect the front-end and back-end.

### Next steps for the PoC

- Sketch and prototype the user's interaction. Keep it simple (no voice detection) and reflect on the relevance of the features for a museum visitor.
- Implement the front-end of the application with HTML, CSS, and JS.
- Implement the back-end of the application with Flask.
- Connect the front-end and back-end.

 
