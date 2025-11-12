
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
### DEVELOPED BY: JAYASREE R
### REGISTER NO: 212223230087

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'AHALYA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image

<img width="788" height="174" alt="Screenshot 2025-11-12 114536" src="https://github.com/user-attachments/assets/8ef35077-2ef1-4660-8653-64f4e162d095" />

### Display the result of Opening
<img width="731" height="149" alt="Screenshot 2025-11-12 114543" src="https://github.com/user-attachments/assets/c11b919e-ee94-4b5e-8343-43d7b5c72a0a" />

### Display the result of Closing
<img width="728" height="158" alt="Screenshot 2025-11-12 114549" src="https://github.com/user-attachments/assets/726a3680-abf6-4e21-bf85-98df26cbc0ac" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
