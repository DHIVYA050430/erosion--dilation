# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.
 
## Program:

``` Python
# Developed By: ARSHITHA MS
# Register No: 212223240015


import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,700),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'ANU RADHA N' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')


```
## Output:

### Display the input Image

![dip 1](https://github.com/user-attachments/assets/e87753eb-aa0a-4894-952f-ea7e2add4378)

### Display the Eroded Image
![dip 2](https://github.com/user-attachments/assets/732dc3d3-64f8-4ba5-9229-b2c34a197ca0)


### Display the Dilated Image
![dip 3](https://github.com/user-attachments/assets/f929e55a-f3e8-461d-a30f-12433c12dcad)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
