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
```python
Developed By:Surothaaman
Register Number: 212222103003
```
## Input Grayscale Image and Color Image :
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("eagle.jpeg")
color_image = cv2.imread("stone.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image :
```python
import numpy as np
import cv2
Gray_image = cv2.imread("eagle.jpeg")
Color_image = cv2.imread("stone.jpg")
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
## Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("eagle.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![exp3dip1](https://github.com/surothaaman/Histogram-of-an-images/assets/133313653/eaaddb3b-7159-459d-bf5d-9b044e09123b)



### Histogram of Grayscale Image and any channel of Color Image
#### Gray Scale -
![exp3dip2](https://github.com/surothaaman/Histogram-of-an-images/assets/133313653/ba3a8a3e-dd30-4ff9-b7f3-d20705c22d6c)

#### Colour Image -
![Screenshot 2024-03-06 000702](https://github.com/sivabalan28/Histogram-of-an-images/assets/113497347/d5495fca-4216-4bb7-887b-1f95b96ecf27)
![Screenshot 2024-03-06 000720](https://github.com/sivabalan28/Histogram-of-an-images/assets/113497347/2662b1b8-d177-474b-973f-e79dc9adbde9)

### Histogram Equalization of Grayscale Image.
![exp3dip4](https://github.com/surothaaman/Histogram-of-an-images/assets/133313653/747c3af0-aa5c-493d-a5f1-27506814b249)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
