## EX NO : 10
## Date : 
# <p align="center"> Implementation of Erosion and Dilation </P>

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:
```
Developed by : P.Suganya
Registeration Number:212220230049
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"SUGANYA",(5,70),font,2,(255),5,cv2.LINE_AA)
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

![o1](https://user-images.githubusercontent.com/77089743/172055653-96aeb217-33db-4e6f-ad8a-551b212ea167.PNG)

</br>
</br>

### Display the Eroded Image

![o3](https://user-images.githubusercontent.com/77089743/172055658-1dd69cf0-d725-432a-8c2f-a524f5265ccb.PNG)


### Display the Dilated Image

![o2](https://user-images.githubusercontent.com/77089743/172055660-8e80d698-1403-403c-8290-952ae3ecf403.PNG)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
