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



![](chenguanxi_1.gif)

Youtube demo:

https://www.youtube.com/watch?v=krfdHI08rI0&feature=youtu.be

详细介绍请参见我的细节文章:

[用AI技术进行换脸（洪山陈冠希的诞生）](https://mp.weixin.qq.com/s?__biz=MzI4MTAyMzQ2OA==&mid=2650679493&idx=1&sn=8b34239595dd02c75479fd621bfce5f3&chksm=f3a50e46c4d287502016b1022921507991838412ad69c97545afb76e1a5e55258e1690ac4cc0#rd)
