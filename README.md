# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

 
## Program:
```
Developed by: Parshwanath M
Register number: 212221230073
```

``` 
# Import the necessary packages
import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Parsh",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("ORIGINAL IMAGE")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
open_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("OPENING")
plt.imshow(open_image)
plt.axis('off')

# Use Closing Operation
close_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("CLOSING")
plt.imshow(close_image)
plt.axis('off')
```

## Output:

### Display the input Image
![@1](https://github.com/parsh2004/Opening-and-Closing/assets/95388047/cddddf6d-3baf-439f-b82e-caf0d9e4ef6d)

### Display the result of Opening
![@2](https://github.com/parsh2004/Opening-and-Closing/assets/95388047/b798a959-4674-45d0-b045-65ed8dca2112)

### Display the result of Closing
![@3](https://github.com/parsh2004/Opening-and-Closing/assets/95388047/ab926083-5d4e-4f20-a43f-30fa0f300231)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
