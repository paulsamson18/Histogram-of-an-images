# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: Paul Samson.S
# Register Number: 212222230104
```
### Grayscale image and Color image
```python

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("dala2.jpeg")
color_image = cv2.imread("vijay.jpeg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```



### Histogram of Grayscale Image and any channel of Color Image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("dala2.jpeg")
Color_image = cv2.imread("vijay.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```


### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("dala2.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### OUTPUT
## Input Grayscale Image and Color Image
![image](https://github.com/Safeeq-Fazil/Histogram-of-an-images/assets/118680361/930fcd41-c0a6-4e1c-905c-4171e2bbba6a)

![image](https://github.com/Safeeq-Fazil/Histogram-of-an-images/assets/118680361/baadd794-bc63-4b93-8324-a6b2ac34e12f)

## Histogram of Grayscale Image and any channel of Color Image
## Grayscale image
![image](https://github.com/Safeeq-Fazil/Histogram-of-an-images/assets/118680361/46e4e477-4434-4399-a9a4-1f89efcf2eee)
![image](https://github.com/Safeeq-Fazil/Histogram-of-an-images/assets/118680361/0b350b47-2996-4d40-84c3-95a21a2a55cd)

## Color image
![image](https://github.com/Safeeq-Fazil/Histogram-of-an-images/assets/118680361/049807fa-4826-4abe-b58b-a3e15ee04c36)
![image](https://github.com/Safeeq-Fazil/Histogram-of-an-images/assets/118680361/0336a2e1-6088-4ffa-904f-04d83e678f01)

## Histogram Equalization of Grayscale Image.
![image](https://github.com/Safeeq-Fazil/Histogram-of-an-images/assets/118680361/a6cf7ea8-1cda-4a28-93eb-de2a0169c383)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
