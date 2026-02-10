# Exp-6

### Developed by: SHARON STEFFANI.F
### Register Number: 212223110049
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

## Program:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

import cv2
import numpy as np
import matplotlib.pyplot as plt


image = cv2.imread('sharon .jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

```

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:




<img width="326" height="453" alt="image" src="https://github.com/user-attachments/assets/cb40a7ab-d3ab-4fc3-9c1f-dbf8ee139c0b" />











<img width="338" height="455" alt="image" src="https://github.com/user-attachments/assets/f445daf1-74cc-44d1-acf9-0464f299c524" />










<img width="339" height="459" alt="image" src="https://github.com/user-attachments/assets/b9b92a27-c6dd-4d2d-bdf3-71d461eaa03b" />








<img width="324" height="438" alt="image" src="https://github.com/user-attachments/assets/15cae45c-76ba-4924-a08e-d94267d8f0bf" />




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
