# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary modules.

### Step 2:
Average filter
```python3
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
```
Weighted average filter
```python3
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
```
Gaussian Blur
```python3
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
Median filter
median=cv2.medianBlur(image2,13)
```
### Step 3:
For performing sharpening on a image.
Laplacian Kernel
```python3
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
```
Laplacian Operator
```python3
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
```
### Step 4:
Display all the images with their respective filters. 

## Program:
### Developed By   : N Sandhya Charu
### Register Number: 212220230041
```python3
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("image.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
### 1. Smoothing Filters

### i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
### ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
### iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
### iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
### i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
### ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
### i) Using Averaging Filter
![image](https://user-images.githubusercontent.com/75235167/167540524-8965b566-4d51-4ac5-ab70-542095a8d4ae.png)
### ii) Using Weighted Averaging Filter
![image](https://user-images.githubusercontent.com/75235167/167540567-1e772896-faf1-4e3d-847c-2d2a9138af3e.png)
### iii) Using Gaussian Filter
![image](https://user-images.githubusercontent.com/75235167/167540592-2ce707c2-99f6-46a7-82d0-d816df0b5f0b.png)
### iv) Using Median Filter
![image](https://user-images.githubusercontent.com/75235167/167540626-8d1572b6-9ed1-48d6-a66f-527f4413cc66.png)
### 2. Sharpening Filters
### i) Using Laplacian Kernal
![image](https://user-images.githubusercontent.com/75235167/167540654-9d54d8e6-c03a-4c50-acdd-d9027f78d588.png)
### ii) Using Laplacian Operator
![image](https://user-images.githubusercontent.com/75235167/167540683-060ff009-4a4a-4211-b969-43ef6066f8b4.png)
## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
