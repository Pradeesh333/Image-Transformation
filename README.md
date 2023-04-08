# Image-Transformation

## Aim

To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:

Anaconda - Python 3.7

## Algorithm:

### Step1:

Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step2:

Translate the image.
<br>

### Step3:

Scale the image.
<br>

### Step4:

Shear the image.
<br>

### Step5:

Reflect of image.
<br>

### Step6:

Rotate the image.
<br>

## Program:

```python
Developed By: Pradeesh S
Register Number: 212221240038

i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt

image=cv2.imread("Gojo-Satoru.jpg",1)
image=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()

rows,cols,dim=image.shape
M=np.float32([[1,0,100],[0,1,100],[0,0,1]])
trans_image=cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(trans_image)
plt.show()


ii) Image Scaling

S=np.float32([[4,0,0],[0,4,0],[0,0,4]])
scaled_image=cv2.warpPerspective(image,S,(cols*4,rows*4))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()

iii)Image shearing

M_x=np.float32([[1,0.9,0],[0,1,0],[0,0,1]])
M_y=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
shearX_image=cv2.warpPerspective(image,M_x,(cols*2,rows*2))
shearY_image=cv2.warpPerspective(image,M_y,(cols*2,rows*2))
plt.axis('off')
plt.imshow(shearX_image)
plt.show()


plt.imshow(shearY_image)
plt.show()

iv)Image Reflection

M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()


v)Image Rotation

angle=np.radians(80)
M=np.float32([[np.sin(angle),-(np.cos(angle)),0],
               [np.cos(angle),np.sin(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()


vi)Image Cropping

cropped_img=image[200:250,400:650]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()



```

## Output:

### i)Image Translation

![](op1.png)

### ii) Image Scaling

![](op2.png)

### iii)Image shearing

![](op3.png)

### iv)Image Reflection

![](op4.png)

### v)Image Rotation

![](op5.png)

### vi)Image Cropping

![](op6.png)

## Result:

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
