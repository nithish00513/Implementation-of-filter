# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1

 Import the required libraries.

## Step2

 
Convert the image from BGR to RGB.

## Step3

Apply the required filters for the image separately.

## Step4

Plot the original and filtered image by using matplotlib.pyplot.

## Step5

End the program.



## Program:
### Developed By   : nithish kumar
### Register Number: 21222224230190


## 1. Smoothing Filters

### i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("paris.jpg")
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


### ii) Using Weighted Averaging Filter

```
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

```
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

```
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

## 2. Sharpening Filters

###  i) Using Laplacian Kernal
```

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

```
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

## i) Using Averaging Filter

<img width="1021" height="362" alt="image" src="https://github.com/user-attachments/assets/0f5a0cb4-b67a-41e3-b3c1-e111ca4af7e4" />



## ii) Using Weighted Averaging Filter

<img width="755" height="260" alt="image" src="https://github.com/user-attachments/assets/ab2d8de8-1b36-4091-aa5f-c1f19ce78243" />



## iii) Using Gaussian Filter

<img width="668" height="291" alt="image" src="https://github.com/user-attachments/assets/ed4306a5-4cc3-4d1a-b56c-33a6972abb9b" />





## iv) Using Median Filter

<img width="901" height="357" alt="image" src="https://github.com/user-attachments/assets/c891cf09-bc61-4a3e-ad90-13c193af2710" />


### 2. Sharpening Filters


## i) Using Laplacian Kernal

<img width="650" height="299" alt="image" src="https://github.com/user-attachments/assets/1cf33313-0544-4a25-abde-421e256ca3ff" />








## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
