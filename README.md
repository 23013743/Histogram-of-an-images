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
# Developed By: Nirmal N
# Register Number: 212223240107
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('a.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```
  
## Output:
### Input Grayscale Image and Color Image

<img width="205" height="278" alt="Screenshot 2026-02-19 094151" src="https://github.com/user-attachments/assets/87978f11-4e4d-4bf4-b523-d53037f07e61" />

<img width="238" height="281" alt="Screenshot 2026-02-19 094200" src="https://github.com/user-attachments/assets/db6ce030-3f17-4b99-beaa-11079fcc2296" />




### Histogram of Grayscale Image and any channel of Color Image


<img width="413" height="304" alt="Screenshot 2026-02-19 094210" src="https://github.com/user-attachments/assets/aa37ae38-09c7-4049-8845-e12a3a65b48a" />




### Histogram Equalization of Grayscale Image.

<img width="402" height="297" alt="Screenshot 2026-02-19 094216" src="https://github.com/user-attachments/assets/3794348e-c07f-40f2-9123-c0603568c5a6" />





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
