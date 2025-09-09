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
### Developed By   : ibrahim fedah s
### Register Number: 212223240056

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("img0.jpg")
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
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv)Using Median Filter
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
i) Using Laplacian Linear Kernal
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
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
## original image:
<img width="717" height="252" alt="download" src="https://github.com/user-attachments/assets/9a7ee386-2125-497c-bbeb-aaaf37339a3a" />


### 1. Smoothing Filters

## i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/eb3b734c-5842-4314-9a97-b95b7b2fb6dd)


## ii)Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/82bafb87-03ac-4da3-967f-121325904006)



## iii)Using Gaussian Filter
![image](https://github.com/user-attachments/assets/92919bb9-09bb-4875-9df2-74038da4816b)




## iv) Using Median Filter
![image](https://github.com/user-attachments/assets/ec4e3f65-0290-4e2f-b02d-99159d5a73d1)





### 2. Sharpening Filters
</br>

## i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/2a268cb3-e908-4963-a321-42848edc3aa4)



## ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/57ddfb34-961e-4135-9185-73e98c7eb67c)




## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.



