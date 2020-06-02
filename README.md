# Traffic signs detection and classification in real time

### 1. Description ###
This project is a traffic signs detection and classification system on videos using OpenCV.
The detection phase uses Image Processing techniques that create contours on each video frame and find all ellipses or circles among those contours. They are marked as candidates for traffic signs.

The SVM Model is trained each time the ```main.py``` called, before the detection phase but I still save the model in [data_svm.dat](data_svm.dat) to implement the model-reload function in the future to avoid retraining phase.
### 2. Prerequisites:
- Python 3.5
- [OpenCV3](https://opencv.org/)
- Imutils (use```pip3 install imutils``` to install)

### 3. System structure
##### a. There are 3 python files as 3 modules:
- [main.py](main.py) :The start point of the program.
- [classification.py](classification.py) :SVM Model to classify traffic signs
- [common.py](common.py) :Functions for defining SVM Model

Other files:
- [data_svm.dat](data_svm.dat) : Saved SVM model after training.
- [README.md](README.md) : This file, obiviously :)

##### b. [Dataset](dataset)
The [Dataset](dataset) folder contains images for training SVM models. There are 12 folders contains cropped images of traffic signs. Each folder is named as the class of the traffic signs it contains. The special [0](dataset/0) folder contains non-traffic-sign cropped images which can be recognized as traffic signs in the detection phase. 
![Wrong detected traffic signs](images/0.png
### 4.  How to run?
Use default arguments on command prompt: python main.py
### 5.Result
![](images/demo.gif)
