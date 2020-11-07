# SuperSaiyanAR
Super Saiyan Augmented Reality With OpenCV and Dlib

## Prerequisites

Install: OpenCV,  Dlib and Gif2Numpy

```
pip install opencv-python
pip install dlib 
pip install gif2numpy
```

Download: CNN Dlib Face Detector - [mmod_human_face_detector.dat](http://dlib.net/files/mmod_human_face_detector.dat.bz2)

## Run

After connecting the **webcam**, run the following scripts:-

```
python3 cnn_face_detect.py # Run cnn face detector
python3 facial_landmarks.py # Run facial landmarks predictor
python3 hairar.py # Run super saiyan ar application
```

**Note**: In the AR application, open your **mouth** to activate supersaiyan animations.

## Dlib Facial Landmarks

![Screenshot](dlib_facial_landmarks.png)

* The **center point** of the hair and aura images were calculated using the location of  landmark points **27** and **30**.
* The **width** of the overlay images were calculated based on distance between landmark points **0** and **16**.
* To check if the **mouth** is opened, we compare the average distance of **lip landmark** points: [(50,61),(51,62),(52,63)]
with average distance of **mouth landmark** points: [(61,67), (62, 66), (63, 65)].
* For animating the **aura glow**, four consecutive frames of the original **animated gif** were used for overlay in a cyclical order.
