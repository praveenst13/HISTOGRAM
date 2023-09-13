# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image

### Step2:

Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:

Display the histograms with their respective images.

### Step4:

Equalize the grayscale image.

### Step5:

Display the grayscale image.
## Program: 

# Developed By:Praveen s
# Register Number:212222240077


```python
# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('fox.jpg')
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread('fox.jpg',0)
plt.imshow(Color_image)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("fox.jpg")
color_image = cv2.imread("fox1.png")
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('fox1.png',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image


![dipt1](https://github.com/praveenst13/HISTOGRAM/assets/118787793/b6a81d17-b789-42c4-8588-ac13de800049)



![dipt2](https://github.com/praveenst13/HISTOGRAM/assets/118787793/ed7fa925-ae1d-4815-8058-44ce98cfb0a1)



### Histogram of Grayscale Image and any channel of Color Image

![dipt3](https://github.com/praveenst13/HISTOGRAM/assets/118787793/993bf6d3-b002-45bf-bebf-abada68f9e77)



![dipt4](https://github.com/praveenst13/HISTOGRAM/assets/118787793/d895b197-404b-45fb-bb98-f3046e526d30)


![dipt5](https://github.com/praveenst13/HISTOGRAM/assets/118787793/37e2d4ef-c585-4721-b67c-ef684cf90961)

![dipt6](https://github.com/praveenst13/HISTOGRAM/assets/118787793/c6316297-0263-4864-9960-a1feb9fa950e)

 
### Histogram Equalization of Grayscale Image


![dipt](https://github.com/praveenst13/HISTOGRAM/assets/118787793/8febd64e-557f-41da-bcf9-a8899ddc3481)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
