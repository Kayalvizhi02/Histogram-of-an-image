### EX NO: 04
### DATE:
# <p align="center">Histogram Equalization of an image</p>
## Aim:

To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:

Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:

Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:

Display the histograms with their respective images.

### Step4:

Equalize the grayscale image.

### Step5:

Display the grayscale image.

## Program:
```
Developed By: KAYALVIZHI M
Register Number: 212220230024
```

### Write your code to find the histogram of gray scale image and color image channels.

```python

import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('cat.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

```
### Display the histogram of gray scale image and any one channel histogram from color image
```python

import cv2
import matplotlib.pyplot as plt
Color_image=cv2.imread('water.jpg')
plt.imshow(Color_image)
plt.show()
hist=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


```
### Write the code to perform histogram equalization of the image. 
```python

import cv2
Gray_image=cv2.imread('cat.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image

![img](https://user-images.githubusercontent.com/75413726/164894864-15f7baba-324e-4c77-a356-09928ecd75e9.jpg) 
![img1](https://user-images.githubusercontent.com/75413726/164894874-11f4b4c5-a9e0-4791-b960-32e7a9bbafa3.jpg)


### Histogram of Grayscale Image and any channel of Color Image

![img3](https://user-images.githubusercontent.com/75413726/164894967-b7ea6e71-3fe3-4e0d-8eed-3b1f8b7c3349.jpg) 
![img4](https://user-images.githubusercontent.com/75413726/164894981-be3dbccd-545a-4e0b-adc7-ddb2e6f731ca.jpg)


### Histogram Equalization of Grayscale Image

![img2](https://user-images.githubusercontent.com/75413726/164894525-5ad88450-6888-4bc4-b1ef-4cedc37e3911.jpg)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
