# Opening-and-Closing

## Aim:

To implement Opening and Closing using Python and OpenCV.

## Software Required:

1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

### Step 1:

Load the necessary packages requiured for the implemtation of opening and closing.

### Step 2:

Create the text image for the implemtation of opening and closing using cv2.putText function.

### Step 3:

Create the structuring image for the implemtation of opening and closing on the text image.

### Step 4:

Apply the erosion and dilation to the text image using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:

Display the images of the erosion and dilation applied using the plt.imshow.

### Step 6:

End the program.
 
## Program:

``` python

# Import the necessary packages:

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText:

text_image = np.zeros((100,300),dtype = 'uint8')
font = cv2.FONT_HERSHEY_TRIPLEX = 7
cv2.putText(text_image,"Sanjay",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element:

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(8,8))

# Use Opening operation:

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation:

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```

## Output:

### Display the input Image:

![img1](https://github.com/Sanjay-shankar-ai/Opening-and-Closing/assets/94231938/a1ede672-2d73-4bd1-966a-0ad0281d3248)

### Display the result of Opening:

![img2](https://github.com/Sanjay-shankar-ai/Opening-and-Closing/assets/94231938/db0f4976-2388-4374-ac5f-0652682c580b)

### Display the result of Closing:

![img3](https://github.com/Sanjay-shankar-ai/Opening-and-Closing/assets/94231938/8bac148e-e07f-449d-87a5-1a2dbbc2e50c)

## Result:

Thus the Opening and Closing operation is used in the image using python and OpenCV.

