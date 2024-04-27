# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result
### Step4:

Similarly, perform closing operation and display the result

### Step5:
End the program.


 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt



# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'ORANGE',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis('off')


# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")

# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")





```
## Output:

### Display the input Image

![image](https://github.com/Goutham2306/OPENING--AND-CLOSING/assets/138971154/5905db22-03f4-4a7c-9a13-9a97c6b4272c)


### Display the result of Opening

![image](https://github.com/Goutham2306/OPENING--AND-CLOSING/assets/138971154/8a25ede4-0346-456d-8bef-06d9cd25be8b)


### Display the result of Closing

![image](https://github.com/Goutham2306/OPENING--AND-CLOSING/assets/138971154/161cc4de-e163-496f-80ba-265e64284976)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
