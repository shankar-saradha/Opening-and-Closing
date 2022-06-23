# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
 Import the necessary packages.
<br>


### Step2:
Create the Text using cv2.putText.
<br>

### Step3:
Create the structuring element.
<br>

### Step4:
Use Opening operation.
<br>

### Step5:
Use Closing Operation.
<br>

### Step6:
Print the output and end the program.
<br>

 
## Program:

``` Python
import cv2
import numpy as np 
import matplotlib.pyplot as plt 
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Shankar",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')





```
## Output:

### Display the input Image
![download](https://user-images.githubusercontent.com/93978702/175304880-acff9e62-f4b5-4c85-8994-7c67d1cfcea2.png)

<br>


### Display the result of Opening
![download](https://user-images.githubusercontent.com/93978702/175304910-079a9e8a-3a1d-4527-8f21-6ebe7ef5b869.png)

<br>


### Display the result of Closing
![download](https://user-images.githubusercontent.com/93978702/175304921-d5fc84ed-8ab4-4c52-9497-cf1adac0f54b.png)

<br>


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
