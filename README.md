# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:

### Step1:
Import cv2 and save and image as filename.jpeg

### Step2:
Use imread(filename, flags) to read the file.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By:LOGESHWARI.P
# Register Number:212221230055
# i) Convert BGR and RGB to HSV and GRAY

import cv2
house_color_image = cv2.imread('image.jpeg')
cv2.imshow('Original image', girl_color_image)
hsv_image = cv2.cvtColor(girl_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (girl_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
girl_color_image = cv2.imread('image.jpeg')
cv2.imshow('Original image', girl_color_image)
hsv_imagel = cv2.cvtColor(girl_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' , hsv_imagel)
gray_image = cv2.cvtColor(girl_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow( 'HSV2BGR', gray_image)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
house_color_image = cv2.imread('image.jpeg')
cv2.imshow('Original image', girl_color_image)
hsv_imagel = cv2.cvtColor(girl_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb' , hsv_imagel)
gray_image = cv2.cvtColor(girl_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow( 'BGR2YCrCb', gray_image)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('image.jpeg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image


import cv2
image = cv2.imread('image.jpeg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()
S
```
## Output:
### i) BGR and RGB to HSV and GRAY
![DIP3A](https://user-images.githubusercontent.com/94211349/228280735-cd79277d-1f5c-4b4a-bf90-53821f8c1584.png)

### ii) HSV to RGB and BGR
![DIP3B](https://user-images.githubusercontent.com/94211349/228280837-797d5a50-203b-4648-bb81-54e1da06ae4b.png)

### iii) RGB and BGR to YCrCb
![DIP3C](https://user-images.githubusercontent.com/94211349/228280933-067a7ab2-e3c7-4a9d-bb0a-4772b9a2c203.png)

### iv) Split and merge RGB Image
![DIP3D](https://user-images.githubusercontent.com/94211349/228281011-406611a7-c87c-4a47-a42b-f851bc751963.png)

### v) Split and merge HSV Image
![DIP3E](https://user-images.githubusercontent.com/94211349/228281070-c2acd8cc-7856-449f-9177-6a5cf1b55be3.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
