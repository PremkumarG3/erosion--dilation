# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br> Import the neccesary packages
### Step2:
<br> creat the text using cv2.put Text

### Step3:
<br> Create the structuting element

### Step4:
<br>  Erodde the image

### Step5:
<br> Dilate the image
 
## Program:
### Name: PREM KUMAR G
### Register Number: 212223230158
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((300,700), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='HAREVASU', org=(50,200), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img,title="Original Image"):
    fig=plt.figure(figsize=(10,8))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    ax.set_title(title, fontsize=16)
    plt.show()

img = load_img()
display_img(img)

kernal = np.ones((5,5),dtype=np.uint8)

img1 = cv2.erode(img,kernal,iterations = 2)
display_img(img1,"Eroded Image")

dilate = cv2.dilate(img,kernal,iterations = 3)
display_img(dilate,"Dilated Image")
```
## Output:
### Display the input Image

![alt text](<DIP 9.1.png>)

### Display the Eroded Image

![alt text](<DIP 9.2.png>)

### Display the Dilated Image

![alt text](<DIP 9.3.png>)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
