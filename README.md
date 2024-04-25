# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.
### Step2

Convert the image from BGR to RGB.

### Step3

Apply the required filters for the image separately.

### Step4

Plot the original and filtered image by using matplotlib.pyplot.

### Step5

End the program.

## Program:
### Developed By   : CHAITANYA P S
### Register Number: 212222230024
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("car.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
ii) Using Weighted Averaging Filter
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
iii) Using Gaussian Filter
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

iv) Using Median Filter
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
i) Using Laplacian Kernal
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
ii) Using Laplacian Operator
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

i) Using Averaging Filter

![download](https://github.com/chaitanya18c/Implementation-of-filter/assets/119392724/8355f060-1e54-40b5-88df-7d6a3396e7af)


ii) Using Weighted Averaging Filter

![download](https://github.com/chaitanya18c/Implementation-of-filter/assets/119392724/bd3378b5-4c3f-4151-8eeb-79430d87eaa3)


iii) Using Gaussian Filter

![download](https://github.com/chaitanya18c/Implementation-of-filter/assets/119392724/220c869d-35ce-4d21-8529-31ccea78984a)


iv) Using Median Filter

![download](https://github.com/chaitanya18c/Implementation-of-filter/assets/119392724/5702e9e7-60c5-4822-9d80-3fe677e7a354)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![download](https://github.com/chaitanya18c/Implementation-of-filter/assets/119392724/df4e1471-ca42-4e8f-92ac-b7c7d9110157)


ii) Using Laplacian Operator

![download](https://github.com/chaitanya18c/Implementation-of-filter/assets/119392724/ddc33bc8-c1ff-46b6-bf6a-674963b4cb12)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
