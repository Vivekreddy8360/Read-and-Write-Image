# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
```python
# Developed By: Vivek Reddy
# Register Number: 212221240030
# To Read,display the image

import cv2
colorImage = cv2.imread('/Users/eswar1607/Desktop/flower.png',1)
cv2.imshow('212221240030-Read&Display',colorImage)
cv2.waitKey(0)

# To write the image

import cv2
colorImage = cv2.imread('/Users/eswar1607/Desktop/flower.png',1)
cv2.imwrite('/Users/eswar1607/Desktop/written.jpg',colorImage)
writtenImage = cv2.imread('/Users/eswar1607/Desktop/written.jpg',1)
cv2.imshow('212221240030-WrittenImage',writtenImage)
cv2.waitKey(0)

# Find the shape of the Image

import cv2
colorImage = cv2.imread('/Users/eswar1607/Desktop/flower.png',1)
print(colorImage.shape)

# To access rows and columns

import cv2
import random
colorImage = cv2.imread('/Users/eswar1607/Desktop/flower.png',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow('212221240030-AccessingRowsAndColumns',colorImage)
cv2.waitKey(0)

# To cut and paste portion of image

import cv2
color_img = cv2.imread('/Users/eswar1607/Desktop/flower.png',1)
tag = color_img[100:300,200:400]
color_img[500:700,400:600] = tag
cv2.imshow('212221240030-CutAndPaste',color_img)
cv2.waitKey(0)

```
## Output:

### i) Read and display the image

<br>
<img width="601" alt="Screenshot 2022-03-30 at 9 38 56 PM" src="https://user-images.githubusercontent.com/94525701/160883067-f238d01b-18ef-4653-8998-ebdd4cd07269.png">
<br>

### ii)Write the image

<br>
<img width="601" alt="Screenshot 2022-03-30 at 9 39 59 PM" src="https://user-images.githubusercontent.com/94525701/160883101-ed609a67-5d74-497b-a934-a9d78db3abc0.png">
<br>

### iii)Shape of the Image

<br>
<img width="803" alt="Screenshot 2022-03-30 at 9 41 16 PM" src="https://user-images.githubusercontent.com/94525701/160883132-d8992b6f-7920-42e4-ab78-7ae4ae330a9d.png">
<br>

### iv)Access rows and columns
<br>
<img width="601" alt="Screenshot 2022-03-30 at 9 42 35 PM" src="https://user-images.githubusercontent.com/94525701/160883161-fb305e39-55f7-43b5-91e6-1c41a225266b.png">
<br>

### v)Cut and paste portion of image
<br>
<img width="601" alt="Screenshot 2022-03-30 at 9 45 00 PM" src="https://user-images.githubusercontent.com/94525701/160883200-9be1c915-6bab-4a52-b586-f33279592ae3.png">
<br>

## Result:
Thus the images are read, displayed, and written successfully using the python program.
