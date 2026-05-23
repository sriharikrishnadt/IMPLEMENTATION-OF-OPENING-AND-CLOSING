# OPENING--AND-CLOSING
### Name - SRI HARI KRISHNA D T
### Register Number - 212224240160
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


## Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
## Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
## Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'SANTHOSH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
## Create the structuring element
```
kernel = np.ones((3, 3), np.uint8)
```
## Display the input image
```
print("SRI HARI KRISHNA D T")
print("212224240160")
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```

## Opening is erosion followed by dilation
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
## Display the result of Opening
```
print("SRI HARI KRISHNA D T")
print("212224240160")
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')

```



## Closing is dilation followed by erosion
```
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Display the result of Opening
```
print("SRI HARI KRISHNA D T")
print("212224240160")
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
# Output:

### Display the input Image

<img width="748" height="647" alt="image" src="https://github.com/user-attachments/assets/c122a7e0-289a-43a5-aabf-1dbe81767bbd" />



### Display the result of Opening

<img width="797" height="649" alt="image" src="https://github.com/user-attachments/assets/109c27f4-0afb-4a6f-8211-d5a14650e449" />



### Display the result of Closing

<img width="756" height="681" alt="image" src="https://github.com/user-attachments/assets/a292e61c-0343-44ba-aaf9-21514ce26e33" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
