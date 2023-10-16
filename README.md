# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>
### Step2:
Create the Text using cv2.putText.
<br>
### Step3:
Create the structuring element.
<br>
### Step4:
Use Opening operation
<br>
### Step5:
Use Closing Operation
<br>
## Program:
```
Developed by:ROSHINI RK
Register Number:212222230123
```

# Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
``` Python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(img1,'ROSHINI RK',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Create the structuring element
``` Python
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()
```

# Use Closing Operation

``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image
<br>

![image](https://github.com/roshiniRK/OPENING--CLOSING/assets/118956165/75146bb5-ec22-414e-878a-fd7fb8292299)


<br>

### Display the result of Opening
<br>

![image](https://github.com/roshiniRK/OPENING--CLOSING/assets/118956165/8bef1ec3-30cc-4cdf-95fa-5be962f41faf)


<br>

### Display the result of Closing
<br>

![image](https://github.com/roshiniRK/OPENING--CLOSING/assets/118956165/19903e66-b4cb-45f6-9ed2-c303f04c1134)


<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
