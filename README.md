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
## program 
Name: Himavath M
Register Number: 212223240053
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Fish.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)  
sobel_edge = cv2.magnitude(sobel_x, sobel_y)  
laplacian_edge = cv2.Laplacian(gray_image, cv2.CV_64F) 
canny_edge = cv2.Canny(gray_image, 100, 200)  
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)
sobel_edge = cv2.magnitude(sobel_x, sobel_y)
sobel_edge = cv2.convertScaleAbs(sobel_edge)
sobel_edge = cv2.magnitude(sobel_x, sobel_y)  
laplacian_edge = cv2.Laplacian(gray_image, cv2.CV_64F) 
canny_edge = cv2.Canny(gray_image, 100, 200)  
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)
sobel_edge = cv2.magnitude(sobel_x, sobel_y)
sobel_edge = cv2.convertScaleAbs(sobel_edge)

plt.figure(figsize=(8, 6))
plt.subplot(2, 2, 1)
plt.imshow(laplacian_edge, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(canny_edge, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')

plt.subplot(2, 2, 3)
plt.imshow(sobel_edge, cmap='gray')  
plt.title("Sobel Edge Detector")
plt.axis('off')

plt.tight_layout()
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
![image](https://github.com/user-attachments/assets/500459ee-2648-44b1-83fd-f592f330e9fe)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/6e046abe-e3b2-4e14-b367-93135a7e0be9)


### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/8dc99e66-75f2-457f-be03-428695060201)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
