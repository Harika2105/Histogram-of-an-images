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
```
 ## Developed By: S.Harika
## Register Number: 212224240155
```

### Input Grayscale Image and Color Image
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('image.png')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
### OUTPUT:

<img width="488" height="503" alt="Screenshot 2025-09-05 235008" src="https://github.com/user-attachments/assets/ed94e0a2-a507-4aa9-a6b8-eaf31e95cbc8" />


### Histogram of Grayscale Image 
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
### output:

<img width="785" height="530" alt="Screenshot 2025-09-05 235209" src="https://github.com/user-attachments/assets/3f15b9bc-9e9b-4d45-b6d3-092a9d50323e" />

### Histogram Equalization of Grayscale Image.
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
### output:

<img width="558" height="506" alt="Screenshot 2025-09-05 235446" src="https://github.com/user-attachments/assets/dac426e5-a42b-4f41-afa5-1378f5efe067" />

## Equalized Histogram
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

## output:

<img width="765" height="544" alt="Screenshot 2025-09-05 235616" src="https://github.com/user-attachments/assets/a3a71846-4f21-4903-9125-e7e8f21ce974" />




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
