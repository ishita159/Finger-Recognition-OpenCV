# Hand Gesture Recognition
• Extract and segment hand region from the video sequence.

• Recognize the number of fingers from the segmented hand region by using Convex Hull.

## Getting Started

How to use
```    
git clone https://github.com/ishita159/Finger-Recognition-OpenCV
```
Run the File hand_gesture_ex2.py
 
## Prerequisites

- Python 3.5
- OpenCV
```
sudo apt-get install python-opencv
```
## Procedure

* Strategy for counting fingers
    * Garb an ROI (Region of interest)
* Then once a hand enters, we can detect change and apply thresholding
* Strategy for counting fingers
		* Once the hand enters the ROI, we will use a Convel Hull to draw a polygon around the hand
		* Using some maths, we'll calculate the center of the hand against the angle of outer points to infer finger count
* The next step is to use thresholding to grab the hand segment from the ROI
* Now that we have the hand segment, the next step is to actually count the fingers behind held up
* We can do this by utilizing a Convex Hull
* A convex hull draws a polygon by connecting points around the most external points in a frame
* In our case, this set of points is actually just our threshold image of a hand. 
* We can expect a general shape of our polygon to be something like 
* Then using a ratio of that distance we create a circle
* Any points outside of this circle far away enough from the bottom, should be extended fingers

## Working 

#### Image-
![Image of segmented hand region](https://github.com/ishita159/Finger-Recognition-OpenCV/blob/master/Capture.png)



