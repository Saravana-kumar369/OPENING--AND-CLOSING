# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1: Load the necessary libraries (cv2, numpy, and matplotlib) for image processing and display.

### Step 2: Generate a blank image and use cv2.putText() to add the text "Digital Image Processing" and "Techniques" on it.

### Step 3: Show the original image with the added text using matplotlib.

### Step 4: Define a 5x5 cross-shaped structuring element using cv2.getStructuringElement() for morphological operations.

### Step 5: Perform the Opening and Closing operations on the image using cv2.morphologyEx() and display the results for both.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText
image = np.zeros((200, 400), dtype=np.uint8)
cv2.putText(image, 'Digital Image Processing', (10, 100), cv2.FONT_HERSHEY_SIMPLEX, 1, 255, 2)
cv2.putText(image, 'Techniques', (10, 150), cv2.FONT_HERSHEY_SIMPLEX, 1, 255, 2)
plt.imshow(image, cmap='gray')
plt.title('Original Image')
plt.axis('off')
plt.show()

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (5, 5))

# Use Opening operation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(opened_image, cmap='gray')
plt.title('After Opening Operation')
plt.axis('off')
plt.show()

# Use Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closed_image, cmap='gray')
plt.title('After Closing Operation')
plt.axis('off')
plt.show()

```
## Output:

### Display the input Image
<br>

![image](https://github.com/user-attachments/assets/c8616f41-6e70-4aad-80fd-55fc242d20ec)

<br>

### Display the result of Opening
<br>

![image](https://github.com/user-attachments/assets/f1019d5d-18a3-415a-a7c6-6e6311ff2843)

<br>

### Display the result of Closing
<br>

![image](https://github.com/user-attachments/assets/87b61286-7c0d-40fb-a472-0fbbd90e1f89)

<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
