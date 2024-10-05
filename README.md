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
```python
# Developed By: Vijayaraj V
# Register Number:212222230174

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('color.png')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [255], [0, 255])
# Plot histogram of the original grayscale image
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

# Plot histogram of the equalized image
hist_equalized = cv2.calcHist([equalized_image], [0], None, [255], [0, 255])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 255])

```
## Output:
### Input Grayscale Image and Color Image
![WhatsApp Image 2024-10-03 at 3 34 26 PM](https://github.com/user-attachments/assets/745f1fa0-8ce8-4770-abd6-e3d9f67b773a)

### Histogram of Grayscale Image and any channel of Color Image
![WhatsApp Image 2024-10-03 at 3 34 26 PM (1)](https://github.com/user-attachments/assets/22b37e1e-a326-4de1-8d03-6c3317f998f2)


### Histogram Equalization of Grayscale Image.
![WhatsApp Image 2024-10-03 at 3 34 10 PM](https://github.com/user-attachments/assets/68729efa-900f-4ef9-b40e-3afe3441fc45)

### Histogram of the equalized image
![WhatsApp Image 2024-10-03 at 3 34 10 PM (1)](https://github.com/user-attachments/assets/ac32a022-7b4e-4bfb-93ed-81ea4903d4a6)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
