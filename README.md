# Research on detection of spiny crown starfish based on deep learning
## Abstraction
  Spiny crown starfish is a kind of marine life that feeds on corals. With the transformation of human environment, the natural enemies of spiny crown starfish are reduced, resulting in the death of coral in a large area. At present, the prevention and control of spiny crown starfish mainly depends on manual prevention and control, and the first step of manual prevention and control is to identify the position of spiny crown starfish in the image. The main research content is the research on the detection of spiny crown starfish based on deep learning. The specific position of spiny crown starfish in the camera image is recognized through target recognition technology, which helps the staff to process spiny crown starfish in this way. For this task, this paper investigates the relevant models of real-time target detection, including yolov1, yolov2, yolov3 and yolox. After continuous analysis and comprehensive consideration, the yolox model is finally selected. This article uses the kaggle help protect the Great Barrier Reef dataset, which is a competition on the prevention and control of spiny crown starfish, including 23500 images in three videos. Based on this data, the yolox nano and yolox-s models are trained. After comparison, it is found that the effect of yolox-s is better
## Method
  The data comes from a photo collection of a competition - to help protect the Great Barrier Reef. In this competition, you will predict the existence and location of spiny crown starfish in underwater image sequences taken at different times and places around the Great Barrier Reef. The form of prediction is a bounding box and the confidence score of each identified starfish. An image may contain zero or more starfish. The data provides three videos, video_ 0、video_ 1、video_ 2. The data divides the three videos into frame by frame pictures. Each video provides about 15000 pictures. There are one or more spiny crown starfish in the pictures. For the starfish position of each picture, the contestant also marks the real frame position, which greatly facilitates the training process in the future. As a real video of divers, when you continuously watch pictures, you can see a continuous video, from bubbles in the water, random schools of fish, and divers shooting at different angles underwater. It is found that the numbers of some picture sets are not continuous. Considering that divers may have a lot of useless information when diving, the picture set has excluded meaningless pictures. The author suspects that part of the missing number was used as the verification set of the competition organizer.
## Code
  The first step is to train the model. We need to configure the environment, import data, prepare validation set and training set, import weight parameters and training model, and then have our model through validation(see [step1](https://baidu.com))
  
  After that, we need to verify whether our model meets the indicators we need. We need to submit our model to the competition, so that we can get an F2 score to judge whether our model meets the expectations.(see [step2](https://www.kaggle.com/code/yangao888/yolox-inference-on-kaggle-for-cots-lb-0-483/notebook))
