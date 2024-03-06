# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By:VASUNDRA SRI R
# Register Number:212222230168
```
### Input Grayscale Image and Color Image :
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray image.jpg")
color_image = cv2.imread("color image.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

### Histogram of Grayscale Image and any channel of Color Image:
import numpy as np
import cv2
Gray_image = cv2.imread("gray image.jpg")
Color_image = cv2.imread("color image.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

### Histogram Equalization of Grayscale Image:
import cv2
gray_image = cv2.imread("gray image.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-06 195241](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/bd53d265-fdbf-4f1d-aea7-4055bce6c0b9)

![Screenshot 2024-03-06 195257](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/0352cd1a-ab42-42be-b464-fb1643a5bb05)



### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-06 195417](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/70a07361-1243-4727-ad37-eb02d93610f0)
![Screenshot 2024-03-06 195505](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/7ce66407-4a11-4157-93fe-2c5b102aacae)
![Screenshot 2024-03-06 195530](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/28b61ac7-b0f6-43ce-be79-e3452c164275)
![Screenshot 2024-03-06 195549](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/f546f011-c63e-4ba6-866e-452436631b2c)


### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-06 195110](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/01d9218b-663a-4054-8580-a7c8ac03d07d)

![Screenshot 2024-03-06 195128](https://github.com/vasundrasriravi/Histogram-of-an-images/assets/119393983/f02a47c4-e75b-442e-9667-f854262cd388)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
