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
# Developed By: POCHI REDDY.P
# Register Number: 212223240115
```
### Input Grayscale Image and Color Image
```
import cv2
gray_img = cv2.imread('gray.jpg')
gray_img = cv2.resize(gray_img,(300,200))
color_img = cv2.imread('nature.jpg')
color_img = cv2.resize(color_img,(300,200))
cv2.imshow("Gray Image",gray_img)
cv2.imshow("Colour Image",color_img)
cv2.waitKey(0)
```
### Histogram of Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('gray.jpg')
color_img = cv2.imread('nature.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
### Histogram of Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('nature.jpg')
color_img = cv2.imread('gray.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
### Histogram Equalization of Grayscale Image.
```
import cv2
gray_img = cv2.imread('gray.jpg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
```
### Output
### Input Grayscale Image and Color Image
![dip 1 1](https://github.com/pochireddyp/Histogram-of-an-images/assets/150232043/d364d1eb-7f9b-4a8c-b14b-75044dd923dd)
### Histogram of Grayscale Image
![image](https://github.com/pochireddyp/Histogram-of-an-images/assets/150232043/662461f9-ef07-41cd-9aac-11f835b6430b)
### Histogram of Color Image
![image](https://github.com/pochireddyp/Histogram-of-an-images/assets/150232043/b48d5072-153b-485f-8590-e472bd101e9d)
### Histogram Equalization of Grayscale Image.
![dip 1 4](https://github.com/pochireddyp/Histogram-of-an-images/assets/150232043/b2eebbff-2967-40f2-be22-0c78bf69137e)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
