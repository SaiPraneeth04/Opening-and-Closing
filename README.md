# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
### Step2:
Create the Text using cv2.putText.
### Step3:
Use Opening operation.

### Step4:
Use Opening operation.
### Step5:
Use Closing Operation.
## Program:
```python
### Developed by: Sai Praneeth K
### Register No: 212222230067
```
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Create the Text using cv2.putText

img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
im=cv2.putText(img1,'sai praneeth',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow ("image",im)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element

Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
cv2.imshow("opening image",image1)
cv2.waitKey(0)
cv2.DestroyAllWindows()

# Use Closing Operation

image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
cv2.imshow("closeing image",image1)
cv2.waitKey(0)
cv2.DestroyAllWindows()
```
## Output:

### Display the input Image
![MODEL](/dip11.1.jpg)
### Display the result of Opening
![MODEL](/dip11.2.jpg)

### Display the result of Closing
![MODEL](/dip11.3.jpg)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.