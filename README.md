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

## **Name:** DIVYA PRIYA S

## **Register No:** 212225240037
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
# Step 2: Read the image and convert to grayscale
image = cv2.imread('Professional Portrait in Black Blazer (1).png')
 # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
 # Convert to grayscale
# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
 # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```
```
# Step 3: Use Global Thresholding to segment the image
# Apply global thresholding with a threshold value of 127
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
```
```
# Step 4: Use Adaptive Thresholding to segment the image
# Apply adaptive thresholding using Gaussian method
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255,
 cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```
```
# Step 5: Use Otsu's method to segment the image
# Apply Otsu's method for optimal thresholding
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```


## Output

### Original Grayscale Image
<img width="1444" height="572" alt="image" src="https://github.com/user-attachments/assets/9fb24902-3bb3-4245-8c56-870bd16357a5" />



### Global Thresholding

<img width="481" height="440" alt="image" src="https://github.com/user-attachments/assets/8de30296-32a6-42cf-99e3-5ca0e998d8bb" />


### Adaptive Thresholding
<img width="856" height="704" alt="image" src="https://github.com/user-attachments/assets/d869d8dc-73a6-44c1-8880-c1d7833a878c" />



### Otsu's Thresholding
<img width="420" height="659" alt="image" src="https://github.com/user-attachments/assets/f837bbe8-89f3-415b-813c-d49fd7458d84" />



## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
