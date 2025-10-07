## Name: Jeffy Brailin T
## Reg.No: 212223040076

# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program

```
# Load the necessary packages


import cv2
import numpy as np
import matplotlib.pyplot as plt


# Read the Image and convert to grayscale

image = cv2.imread('Qn8_thresholding.tif')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')


# Use Global thresholding to segment the image

 #Apply global thresholding with a threshold value of 127
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)


# Use Adaptive thresholding to segment the image

adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)




# Global Thresholding
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()





```
## Output

### Original Image

<img width="177" height="255" alt="image" src="https://github.com/user-attachments/assets/125f43bc-43d8-4d55-a607-94017aa3b30a" />


### Global Thresholding

<img width="217" height="256" alt="image" src="https://github.com/user-attachments/assets/184fac32-43d3-48f0-8b6f-ac846132c929" />


### Adaptive Thresholding

<img width="251" height="250" alt="image" src="https://github.com/user-attachments/assets/9417ca97-d063-46d0-a19c-33d98b769e00" />



### Optimum Global Thesholding using Otsu's Method

<img width="174" height="258" alt="image" src="https://github.com/user-attachments/assets/8455c127-ee2e-47e1-af50-39d7d9620b7c" />



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
