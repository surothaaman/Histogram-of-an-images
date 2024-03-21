# EX-3 Histogram of an images
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


#### Program:
```
### Developed By: SUROTHAAMAN R
### Register Number: 212222103003
```
<table>
  <tr>
    <td width=50%>
      
####  Histogram of Gray scale image and Color image  
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpg")
color_image = cv2.imread("color.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
#### Output:
### Input Grayscale Image and Color Image
![diptgray1]![Screenshot 2024-03-21 235719](https://github.com/surothaaman/Histogram-of-an-images/assets/133313653/60683529-d8e4-4e55-a72e-1ef657f4ba97)s
![color]![Screenshot 2024-03-21 235743](https://github.com/surothaaman/Histogram-of-an-images/assets/133313653/0fd5ee4c-a2fa-4f54-80a2-4539f2ea62fc)

</td>
</tr>



<tr>
  <td width=50%>

### Histogram of Grayscale image and any color image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpg")
Color_image = cv2.imread("color.jpg")
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
</td>
<td>

### Output:
#### Histogram of Grayscale image and any color image
### Grayscale image
![dipt3](https://github.com/deepikasrinivasans/Histogram-of-an-images/assets/119393935/1aa62857-f5cd-4431-bbc0-2885e400b9df)
### Color image
![dipt4](https://github.com/deepikasrinivasans/Histogram-of-an-images/assets/119393935/8b10a4c9-0eef-4c8b-9567-59202db9a672)
</td>
</tr>



<tr>
  <td width=50%>

### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
### Output:
### Histogram Equalization of Grayscale Image.
![grayscaleimagedipt5](https://github.com/deepikasrinivasans/Histogram-of-an-images/assets/119393935/61fba175-9053-47f5-918e-26673ef2906b)
![equalized imagedipt6](https://github.com/deepikasrinivasans/Histogram-of-an-images/assets/119393935/4251001b-3be2-4a5d-8579-72af6c275f3a)
</td>
</tr>
</table>

### Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
