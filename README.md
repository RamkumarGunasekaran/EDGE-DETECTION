# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program
```
Developed By: Ramkumar G
Reg No: 212223220084

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('car image.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

```
## SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

```
##  CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
### ORAGINAL IMAGE
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/aad13b65-8568-4d52-b178-e8af7607c953" />

### SOBEL EDGE DETECTOR

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/481c1c92-7772-49b5-bf00-c4550b5d09a0" />


### LAPLACIAN EDGE DETECTOR

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/2598b687-f748-416a-aca2-ec5045279310" />


### CANNY EDGE DETECTOR
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/38fa6a94-f733-40b1-9002-cf5d8efe206c" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
