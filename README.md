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
# Developed By: YOHESH KUMAR R.M
# Register Number: 212222240118
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat1.jpg")
color_image = cv2.imread("cat2.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("cat1.jpg")
Color_image = cv2.imread("cat2.jpg")
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
```
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
import cv2
gray_image = cv2.imread("cat1.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-19 114404](https://github.com/yoheshkumar/Histogram-of-an-images/assets/119393568/f5f47617-f66d-4bb9-8196-c902c45dec85)
![Screenshot 2024-03-19 114420](https://github.com/yoheshkumar/Histogram-of-an-images/assets/119393568/9cb96bf3-d2d1-4f89-981b-a9ddbb6421cc)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-19 114501](https://github.com/yoheshkumar/Histogram-of-an-images/assets/119393568/a1ca0606-334a-41ba-8150-87fddc7c03e5)
![Screenshot 2024-03-19 114509](https://github.com/yoheshkumar/Histogram-of-an-images/assets/119393568/0106ad19-635b-4e8b-9d62-11f18c448cd9)
![Screenshot 2024-03-19 114532](https://github.com/yoheshkumar/Histogram-of-an-images/assets/119393568/4d005c00-6270-4fd1-9761-0892d4a0ee8b)
![Screenshot 2024-03-19 114541](https://github.com/yoheshkumar/Histogram-of-an-images/assets/119393568/166106e9-a0d3-41bb-8762-a4d9dbc5fe32)


### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-19 112555](https://github.com/yoheshkumar/Histogram-of-an-images/assets/119393568/2b5dfa24-201d-4e68-8a65-5071ad021420)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
