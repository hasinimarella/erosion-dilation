# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages

Step2:
Create an empty window and add text to it

Step3:
create a structuring element

Step4:
Do the operation

Step5:
Show the output image


### Step2:

Create an empty window and add text to it

### Step3:

create a structuring element

### Step4:
import the cv module by command import cv2

### Step5:

The program should be executed in google colab.
 
## Program:

Developed by:Marella Hasini
Registration number:212223240083
``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText
input_image_path = 'flower.png'
color_image = cv2.imread(input_image_path)
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)
edges = cv2.Canny(gray_image, 100, 200)

kernel_size = 5 
kernel = np.ones((kernel_size, kernel_size), np.uint8)

erosion = cv2.erode(edges, kernel, iterations=1)
dilation = cv2.dilate(edges, kernel, iterations=1)

# Create the structuring element
plt.figure(figsize=(15, 10))
plt.subplot(2, 3, 1)
plt.imshow(cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')

plot.show()
# Erode the image
plt.subplot(2, 3, 4)
plt.imshow(erosion, cmap='gray')
plt.title('Erosion')
plt.axis('on')


plt.show()

# Dilate the image
plt.subplot(2, 3, 5)
plt.imshow(dilation, cmap='gray')  # Corrected variable name
plt.title('Dilation')
plt.axis('on')

plt.show()

```
## Output:

## code:
![OUTPUT](<Screenshot 2024-04-16 114531.png>)

### Display the input Image

![OUTPUT](<Screenshot 2024-04-16 114549.png>)

### Display the Eroded Image

![OUTPUT](<Screenshot 2024-04-16 114554.png>)

### Display the Dilated Image

![OUTPUT](<Screenshot 2024-04-16 114601.png>)

## Result

Thus the generated text image is eroded and dilated using python and OpenCV.
