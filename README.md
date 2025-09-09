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
<img width="717" height="252" alt="download" src="https://github.com/user-attachments/assets/0c3c1707-92f5-4248-b019-7a03609a6164" />



### 1. Smoothing Filters

## i) Using Averaging Filter
<img width="717" height="252" alt="download" src="https://github.com/user-attachments/assets/0870a1a6-d01e-4cb2-a15f-c72fb961ed16" />


## ii)Using Weighted Averaging Filter
<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/8d6ba906-42c8-4642-a5cc-6e0ee80f70d5" />




## iii)Using Gaussian Filter
<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/d13584c7-e1fd-461f-8b4a-fbfbd3337f56" />





## iv) Using Median Filter
<img width="717" height="252" alt="download" src="https://github.com/user-attachments/assets/a24899f0-e760-4ebc-a176-4942bef6895b" />





### 2. Sharpening Filters
</br>

## i) Using Laplacian Kernal
<img width="717" height="252" alt="download" src="https://github.com/user-attachments/assets/6e8bdce0-9da7-48dd-8815-6ebf88103534" />



## ii) Using Laplacian Operator
<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/3de209a1-cf37-434d-a499-b64c06b09c69" />





## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.



