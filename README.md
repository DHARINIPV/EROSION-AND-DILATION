# EROSION-AND-DILATION

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
Apply erosion and dilation using plt.erode and plt.dilate.

### Step5:
Plot the images using plt.imshow.

## Program:
```
Developed by : Dharini PV
Register no: 212222240024
```
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
image = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"Dharini PV",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Create the structuring element
```python
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Erode the image
```python
image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Dilate the image
```python
image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image

![Screenshot from 2023-10-10 18-50-39](https://github.com/DHARINIPV/EROSION-AND-DILATION/assets/119400845/ab9b7660-29ed-4e8b-b711-12a93bab6d8f)

### Display the Eroded Image
![Screenshot from 2023-10-10 18-50-12](https://github.com/DHARINIPV/EROSION-AND-DILATION/assets/119400845/e06133da-d6d4-4bb5-b8cd-d7c696396065)

### Display the Dilated Image

![Screenshot from 2023-10-10 18-51-09](https://github.com/DHARINIPV/EROSION-AND-DILATION/assets/119400845/dd39e44a-fbba-4f90-96a1-f2c8afc71aa7)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
