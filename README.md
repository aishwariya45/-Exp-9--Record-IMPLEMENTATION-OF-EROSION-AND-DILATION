# -Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm:
Step1:
import the neccesary packages

Step2:
create the text using cv2.put Text

Step3:
create the structuting element

Step4:
Erodde the image

Step5:
Dilate the image

## Program:

```
import cv2
import numpy as np
from matplotlib import pyplot as plt
imput_image='actor.jpg'
color_image=cv2.imread(imput_image)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
edges=cv2.Canny(gray_image,100,200)
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
erosion=cv2.erode(edges,kernel,iterations=1)
dilation=cv2.dilate(edges,kernel,iterations=1)
plt.figure(figsize=(15,10))
plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('black and white image')
plt.axis('on')
plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('edge segmentation')
plt.axis('on')
plt.subplot(2,3,4)
plt.imshow(edges,cmap='gray')
plt.title('erosion')
plt.axis('on')
plt.subplot(2,3,5)
plt.imshow(edges,cmap='gray')
plt.title('dilation')
plt.axis('on')


```

# OUTPUT:

## Display the input Image:
<img width="488" height="479" alt="image" src="https://github.com/user-attachments/assets/d997c311-2f90-4b57-a784-642bf5ac4a53" />

## Display the Eroded Image:

<img width="573" height="484" alt="image" src="https://github.com/user-attachments/assets/bbe7d4de-d7bc-40ab-81e7-fbf45443c734" />

## Display the Dilated Image:

<img width="558" height="475" alt="image" src="https://github.com/user-attachments/assets/023d815c-41ca-4177-8bfa-8f7ee1ed70f3" />

# RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.


