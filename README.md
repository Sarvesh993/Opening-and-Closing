## Opening-and-Closing
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step 1:
Import the necessary packages.
## Step 2:
Create the Text using cv2.putText.
## Step 3:
Create the structuring element.
## Step 4:
Use Opening operation.
## Step 5:
Use Closing Operation.
## Step 6:
Print the output and end the program.
## Program:
```
Developed By:P.SARVESHVARAN
Register No:212221230090
```
## Import the necessary packages
```
import numpy as np
import matplotlib.pyplot as plt
import cv2
```
## Create the Text using cv2.putText
```
text_image = np.zeros((100,850),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"P.SARVESHVARAN",(130,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')
```
## Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_ELLIPSE,(5,11))
```
## Use Opening operation
```
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')
```
## Use Closing Operation
```
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')
```
## Output:

## Display the input Image
![image](https://github.com/Sarvesh993/Opening-and-Closing/assets/94881923/6908640c-8562-48f3-b144-d1736dff2a18)

## Display the result of Opening
![image](https://github.com/Sarvesh993/Opening-and-Closing/assets/94881923/d20fcc33-7ea0-4fbf-b4a5-18a4b52b0b66)


## Display the result of Closing
![image](https://github.com/Sarvesh993/Opening-and-Closing/assets/94881923/a7cd7307-ec52-4175-bc8b-4e89bddaed63)

## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
