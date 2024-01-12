---
layout: page
title: Group feedback
nav_exclude: true
nav_order: 2
---

[Raw notes (sent by email)](/assets/pdf/group_feedback_notes.pdf){: .btn .btn-purple .fs-5 .mb-4 .mb-md-0 .mr-2 }

## Group A : Human-machine co-improvisation

- An implementation of a [factor oracle for Pure Data](https://github.com/ajwnycct/factorOracle-Pd)
- [Omax](http://recherche.ircam.fr/equipes/repmus/OMax/)
- [Dicy2](https://forum.ircam.fr/projects/detail/dicy2/) and its [video tutorials](https://www.youtube.com/watch?v=xt8-rlqMIQM&ab_channel=Ircam)
- [Festival on co-improvisation](https://improtech.ircam.fr/)
-  Valerio Velardo [Youtube channel](https://www.youtube.com/@ValerioVelardoTheSoundofAI) on machine learning for music 
- [Artemi-Maria Gioti](https://www.artemigioti.com/about.html) was also interested in machine-artist communication and gave a talk in the last Wintersemester for AICA and [here](https://www.youtube.com/watch?v=r5XixsSdGKI&ab_channel=FluidCorpusManipulation) is also an interview where she talks about some implementation details.


> Assayag, G., & Dubnov, S. (2004). Using factor oracles for machine improvisation. Soft Computing, 8(9), 604-610.
Wilson, A. J. (2016). factorOracle: an Extensible Max External for Investigating Applications of the Factor Oracle Automaton in Real-Time Music Improvisation.

> Nika, J., Chemillier, M., & Assayag, G. (2017). Improtek: introducing scenarios into human-computer music improvisation. Computers in Entertainment (CIE), 14(2), 1-27.

> Dubnov, S., Assayag, G., & Cont, A. (2007). Audio oracle: A new algorithm for fast learning of audio structures. In Proceedings of International Computer Music Conference (ICMC). ICMA.



## Group B : Collaborative visual story-telling

- [How to use Stable diffusion locally](https://www.assemblyai.com/blog/how-to-run-stable-diffusion-locally-to-generate-images/)
- [Automatic111 webGUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) : AUTOMATIC111 also provides an API so it should be possible to 
    - Make a history of prompts via some GUI, for example a Python application
    - Send parts of the history as prompt to Stable Diffusion
    - Receive and display the image and save the pair (image, prompt) into the archive/history

You can also access Stable Diffusion and other image generators via an API but if it does not run on your machine you have to pay for it.


## Group C : Emotion recognition for personalized recommendation

- [FER](https://github.com/justinshenk/fer)
- [DeepFace](https://github.com/serengil/deepface)
- [FaceWork](https://facework.app/) : a critical gamification of facial recognition. You can read more about the artist Kyle McDonald that is familiar with the relation between [AI and faces](https://kcimc.medium.com/working-with-faces-e63a86391a93).

## Group D : Virtual archives of clothing artefacts

- [Gaussian splatting](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/) for 3D modelling of items
- [A tutorial](https://www.kaggle.com/code/eliotbarr/fashion-mnist-tutorial) for learning embeddings of (simplistic) fashion item images.
- [PoseNet](https://github.com/google-coral/project-posenet) for estimating poses

> Gu, X., Wong, Y., Shou, L., Peng, P., Chen, G., & Kankanhalli, M. S. (2018). Multi-modal and multi-domain embedding learning for fashion retrieval and analysis. IEEE Transactions on Multimedia, 21(6), 1524-1537.

## Group E : AI-augmented audio guide

- Audio-to-text : [DeepSpeech](https://github.com/mozilla/DeepSpeech) (can run locally) or [Whisper](https://openai.com/research/whisper)  (API calls);
- Question processing : [Langchain](https://www.langchain.com/) or [https://www.llamaindex.ai/](https://www.llamaindex.ai/). My guess is that you will necessary have to call an API for this part;
- Have a look to [Chat with data](https://www.youtube.com/@chatwithdata) and [other tutorials](https://github.com/ksm26/LangChain-Chat-with-Your-Data). Local Large Language Models exist ([llama.cpp](https://python.langchain.com/docs/integrations/llms/llamacpp)) but are heavy to be supported by an embed system like a Raspberry Pi (it is already too heavy for my computer);
- Text-to-speech : I don't know much about it but have a look to [Mozilla TTS](https://github.com/mozilla/TTS), [Google TTS](https://gtts.readthedocs.io/en/latest/), and [coqui-ai TTS](https://github.com/coqui-ai/TTS).
 
