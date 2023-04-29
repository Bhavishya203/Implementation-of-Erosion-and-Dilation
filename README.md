# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

## Step5:
Plot the images using plt.imshow.

## Program:
```
# Import the necessary packages

import cv2
import numpy as np

# Create the Text using cv2.putText
img1 = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Bhavishya',(5,70),font,2,(255),5,cv2.LINE_AA)


# Create the structuring element
cv2.imshow("Name Image",img1)


# Erode the image and Dilate the image

kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
erodeImage = cv2.erode(img1,kernel1)
dilationImage = cv2.dilate(img1,kernel1)
cv2.imshow("Erode Image",erodeImage)
cv2.imshow("Dilated Image",dilationImage)
cv2.waitKey(0)

cv2.destroyAllWindows()
```

## Output:

### Display the input Image
<img width="242" alt="image" src="https://user-images.githubusercontent.com/94679395/235294902-0c20a050-34bd-4871-a6c7-91a07a956fc4.png">


### Display the Eroded Image
<img width="241" alt="lmage1" src="https://user-images.githubusercontent.com/94679395/235294911-ebb847cf-94eb-4267-aceb-e71b59dd8b8e.png">


### Display the Dilated Image
<img width="240" alt="image 2" src="https://user-images.githubusercontent.com/94679395/235294924-b1776e1a-1ebc-4998-a400-cb6e7c275147.png">


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
