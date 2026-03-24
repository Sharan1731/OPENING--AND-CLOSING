# OPENING--AND-CLOSING
### Name - SHARAN G
### Register Number - 212223230203
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image

image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'AJAY', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')




# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
## Output:

### Display the input Image
<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/96146d90-9664-459c-bb08-f32a1475ee4e" />




### Display the result of Opening

<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/fddb1460-771e-4c1f-9905-101bb3f8888d" />


### Display the result of Closing

<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/844fe42f-a016-41ac-aba5-ca7826b61e90" />


<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
