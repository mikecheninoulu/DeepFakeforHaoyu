**Notice:** This repository is mainly based on faceswap

---

# deepfakes_faceswap
Faceswap is a tool that utilizes deep learning to recognize and swap faces in pictures and videos.

## Overview
The project has multiple entry points. You will have to:
 - Gather photos (or use the one provided in the training data provided below)
 - **Extract** faces from your raw photos
 - **Train** a model on your photos (or use the one provided in the training data provided below)
 - **Convert** your sources with the model

### Extract
From your setup folder, run `python faceswap.py extract`. This will take photos from `src` folder and extract faces into `extract` folder.

### Train
From your setup folder, run `python faceswap.py train`. This will take photos from two folders containing pictures of both faces and train a model that will be saved inside the `models` folder.

### Convert
From your setup folder, run `python faceswap.py convert`. This will take photos from `original` folder and apply new faces into `modified` folder.

#### General notes:
- All of the scripts mentioned have `-h`/`--help` options with arguments that they will accept. You're smart, you can figure out how this works, right?!

Note: there is no conversion for video yet. You can use [ffmpeg](https://www.ffmpeg.org) to convert video into photos, process images, and convert images back to video.

## Training Data
**Whole project with training images and trained model (~300MB):**

### Setup
You need a modern GPU with CUDA support for best performance

**Some tips:**

Reusing existing models will train much faster than starting from nothing.  
If there is not enough training data, start with someone who looks similar, then switch the data.