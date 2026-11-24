
# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** HARIHARAN M

**Register No:** 212225240045


### Original Image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Step 2: Read the image and convert to grayscale
image = cv2.imread('PEACOCK.png')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image)  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```
<img width="505" height="450" alt="image" src="https://github.com/user-attachments/assets/b8fa9bbc-cce1-48c4-b309-b5b7edbdb55b" />




### Original Grayscale Image
```
# Grayscale Image
gray_image = cv2.cvtColor(image, cv2.COLOR_RGB2GRAY)  # Convert to grayscale
plt.imshow(gray_image,cmap = 'gray')  # Convert from BGR to RGB for display
plt.title("Grayscale Image")
plt.axis('off')
```
<img width="506" height="452" alt="image" src="https://github.com/user-attachments/assets/3b892dd8-fb97-409c-9de9-8219be3e069c" />



### Global Thresholding
```
# Step 3: Use Global Thresholding to segment the image
# Apply global thresholding with a threshold value of 127
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
# Global Thresholding
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
<img width="502" height="450" alt="image" src="https://github.com/user-attachments/assets/d12a6070-90cf-4018-ad17-ad8efe631936" />



### Adaptive Thresholding

```
# Apply adaptive thresholding using Gaussian method
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
# Adaptive Thresholding
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
<img width="502" height="455" alt="image" src="https://github.com/user-attachments/assets/b72adccc-5440-4c5c-9562-7aff3d97ed24" />


### Otsu's Thresholding
```
# Apply Otsu's method for optimal thresholding
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
# Otsu's Method
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
<img width="502" height="452" alt="image" src="https://github.com/user-attachments/assets/3581f763-2918-442d-b57c-53f418165c03" />




## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
