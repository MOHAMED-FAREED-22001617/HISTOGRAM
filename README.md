# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries

### Step2:
Use cv2.calcHist(images, channels, mask, histSize, ranges[, hist[, accumulate]]) to find the histogram of the image.

### Step3:

Plot the image and its stem plots using the plt.show() and plt.stem() functions.
### Step4:

Equalize the grayscale image (cv2.equalizeHist().)
### Step5:
Print and end the program.
## Program:
```python
Developed By:MOHAMED FAREED F
Register Number:212222230082
# FOR GRAY IMAGE
## code to read and show the input image
import cv2
import matplotlib.pyplot as plt
gray_image =cv2.imread('MESSI.PNG',0)
cv2.imshow('gray_image',gray_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()

# code to find the histogram of the image

hist = cv2.calcHist([gray_image],[0],None,[256],[0,255])

# Display the histogram graph of the image

plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# code to perform histogram equalization of the image. 

equ_g = cv2.equalizeHist (gray_image)

# code to show histogram equalized image. 

cv2.imshow('EQUALIZED IMAGE',equ_g)
cv2.waitKey(0)
cv2.destroyAllWindows()

# code to find the histogram of the equalized image

equal_hist = cv2.calcHist([equ_g],[0],None,[256],[0,255])

# Display the equalized histogram graph of gray scale image

plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(equal_hist)
plt.show()
```
```python
# code to read and show the input image

import cv2
import matplotlib.pyplot as plt
color_image =cv2.imread('MESSI.PNG',-1)
cv2.imshow('color_img',color_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()

# code to calculate the histogram of different channels of color image

hist0 = cv2.calcHist([color_image],[0],None,[256],[0,255]) #channel 0 - blue
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,255]) #channel 1 - green
hist2 = cv2.calcHist([color_image],[2],None,[256],[0,255]) #channel 2 - red

# Display the histogram graph of different channels of color image

#channel 0 - blue
plt.figure()
plt.title("Histogram")
plt.xlabel('blue value')
plt.ylabel('pixel count')
plt.stem(hist0)
plt.show()

#channel 1 - green
plt.figure()
plt.title("Histogram")
plt.xlabel('green value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

#channel 2 - red
plt.figure()
plt.title("Histogram")
plt.xlabel('red value')
plt.ylabel('pixel count')
plt.stem(hist2)
plt.show()







```
## Output:
### Input Grayscale Image and Color Image
![OP-01](https://github.com/MOHAMED-FAREED-22001617/HISTOGRAM/assets/121412904/8bf0e1f8-ef6e-4757-b6b0-2450ac737584)
![OP-05(1)](https://github.com/MOHAMED-FAREED-22001617/HISTOGRAM/assets/121412904/7458774b-3f46-46dd-93db-3a17460f7c62)




### Histogram of Grayscale Image and any channel of Color Image
![OP-02](https://github.com/MOHAMED-FAREED-22001617/HISTOGRAM/assets/121412904/692f4b78-8e51-4cd1-9c78-f97f77a2a6cd)
![OP-06](https://github.com/MOHAMED-FAREED-22001617/HISTOGRAM/assets/121412904/a3b6ff09-52ec-46ed-be64-aebb228ace66)

![OP-07(1)](https://github.com/MOHAMED-FAREED-22001617/HISTOGRAM/assets/121412904/b748e626-d58a-4a44-be6f-43da9b6f14a8)
![OP-08(1)](https://github.com/MOHAMED-FAREED-22001617/HISTOGRAM/assets/121412904/609617c4-10fe-4678-822e-f54bfed08e58)

### Histogram Equalization of Grayscale Image
![OP-03](https://github.com/MOHAMED-FAREED-22001617/HISTOGRAM/assets/121412904/001326d0-d43e-4137-8b2a-30f71e49964e)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
