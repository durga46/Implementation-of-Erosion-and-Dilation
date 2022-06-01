# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Import the necessary packages.


### Step2:
<br>
Create the text image using cv2.putText.

### Step3:
<br>
Then create the structuring image for dilation/erosion.
### Step4:
<br>
Apply erosion and dilation using cv2.erode and cv2.dilate.
### Step5:
<br>
Plot the images using plt.imshow.
 
## Program:
```python
Developed by : DurgaDevi P
Registeration Number:212220230015
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Gowri",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```

## Output:

### Display the input Image
![s1](https://user-images.githubusercontent.com/75235704/171365301-4f85d363-c743-4897-b1be-eee08e503f88.png)

<br>
<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
![Screenshot_707](https://user-images.githubusercontent.com/75235704/171366111-0caa95c1-c057-419f-8c97-9aae502841a3.png)

<br>
<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
![Screenshot_708](https://user-images.githubusercontent.com/75235704/171366151-c03db9d0-30ae-4ab4-ad38-2443dc1381c2.png)


<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
