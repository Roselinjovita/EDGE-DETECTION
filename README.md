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

## PROGRAM:

```
PROGRAM BY : RPSELIN MARY JOVITA.S
DEVELOPED BY: 212222230122
```

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('wat.webp')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### OUTPUT

![Screenshot 2024-10-10 100551](https://github.com/user-attachments/assets/cdb24636-c11f-4426-ad94-c1c67ea17a25)

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

### OUTPUT 

![Screenshot 2024-10-10 100604](https://github.com/user-attachments/assets/586a58c4-0c18-4334-94d8-756a4423c8bb)

### LAPLACIAN EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
plt.imshow(sobel_x, cmap='gray')
plt.title('Sobel_x')
plt.axis('off')
```
### OUTPUT

![Screenshot 2024-10-10 101143](https://github.com/user-attachments/assets/f9ac879d-330e-4e86-bd7d-0cc24d0d89e4)



### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

### OUTPUT
![Screenshot 2024-10-10 100635](https://github.com/user-attachments/assets/d0d77f80-9949-4dc0-8cae-fd8a19f0d082)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
