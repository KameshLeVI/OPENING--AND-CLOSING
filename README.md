# EXP.10 OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
```py
Developed by: Kanishka V S
Register Number: 212222230061
```
### Import the necessary packages
```py
import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```py
img = np.zeros((100, 400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'APPEALING', (5, 70), font, 2, (255), 5, cv2.LINE_AA)
```
### Create the structuring element
```py
kernel = np.ones((7, 7), np.uint8)
```
### Use Opening operation
```py
imgOpening = cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
```
### Use Closing Operation
```py
imgClosing = cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
```
### Display Result:
```py
plt.imshow(img, cmap = 'gray')
plt.axis("off")

plt.imshow(imgOpening, cmap = 'gray')
plt.axis("off")

plt.imshow(imgClosing, cmap = 'gray')
plt.axis("off")
```

## Output:

### Display the input Image

![Screenshot 2024-05-05 173159](https://github.com/KameshLeVI/OPENING--AND-CLOSING/assets/120780633/57879430-049e-455c-8d55-7c3ea054a63c)


### Display the result of Opening
![Screenshot 2024-05-05 173407](https://github.com/KameshLeVI/OPENING--AND-CLOSING/assets/120780633/010cd107-2142-4cf8-b950-011922d413f2)



### Display the result of Closing

![Screenshot 2024-05-05 173413](https://github.com/KameshLeVI/OPENING--AND-CLOSING/assets/120780633/e41b761d-4142-47a8-8c18-0f09107c2c98)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
