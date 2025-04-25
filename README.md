# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>
Convert the image from BGR to RGB
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By   :Durga V
### Register Number: 212223230052
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1 = cv2.imread("panda.jpeg")
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")





```
ii) Using Weighted Averaging Filter
```
kernel = np.ones((11, 11), np.float32) / 121
averaging_image = cv2.filter2D(image2, -1, kernel)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(averaging_image)
plt.title("Averaging Filter Image")
plt.axis("off")
plt.show()






```
iii) Using Gaussian Filter
```
kernel1 = np.array([[1, 2, 1],
                    [2, 4, 2],
                    [1, 2, 1]]) / 16

weighted_average_image = cv2.filter2D(image2, -1, kernel1)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(weighted_average_image)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()






```
iv)Using Median Filter
```
gaussian_blur = cv2.GaussianBlur(image2, (11, 11), 0)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
sharpened_image = cv2.filter2D(gaussian_blur, -1, kernel1)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(sharpened_image)
plt.title("Sharpened Image (Laplacian Kernel)")
plt.axis("off")
plt.show()






```
ii) Using Laplacian Operator
```
laplacian = cv2.Laplacian(image2, cv2.CV_64F)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(laplacian, cmap='gray')
plt.title("Laplacian Operator Image")
plt.axis("off")
plt.show()






```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

![image](https://github.com/user-attachments/assets/2b2f5312-3ea7-49a5-87f9-6de718b4d7d1)

ii)Using Weighted Averaging Filter

![image](https://github.com/user-attachments/assets/b258866d-01d2-4ec3-b6e4-8abc0a1f6673)

iii)Using Gaussian Filter

![image](https://github.com/user-attachments/assets/73c0072f-8193-46e2-a829-a5c211f9b6ea)

iv) Using Median Filter

![image](https://github.com/user-attachments/assets/25a77d16-3d7c-4757-8025-233a29aed099)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![image](https://github.com/user-attachments/assets/05f9aebf-9b25-4285-8714-77fd60375c0e)


ii) Using Laplacian Operator

![image](https://github.com/user-attachments/assets/9280100c-724f-4adc-8bde-28d646d052c6)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
