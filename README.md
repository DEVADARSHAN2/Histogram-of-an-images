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
```
 Developed By: DEVADARSHAN A S
 Register Number: 212222110007
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grey.jpeg")
color_image = cv2.imread("color.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("grey.jpeg")
Color_image = cv2.imread("color.jpeg")
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
gray_image = cv2.imread("grey.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```







## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-19 113804](https://github.com/DEVADARSHAN2/Histogram-of-an-images/assets/119432150/7376165c-52b8-43cd-9b9c-38315146431e)
![Screenshot 2024-03-19 113711](https://github.com/DEVADARSHAN2/Histogram-of-an-images/assets/119432150/9e3224c3-2925-4e66-8787-12636354447c)



### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image
![Screenshot 2024-03-19 114332](https://github.com/DEVADARSHAN2/Histogram-of-an-images/assets/119432150/beef485c-3f60-4534-987f-d030ecb424fd)
![Screenshot 2024-03-19 114343](https://github.com/DEVADARSHAN2/Histogram-of-an-images/assets/119432150/bf5ebc6d-de69-4cba-b04f-9259c8432b57)

#### Color Image
![Screenshot 2024-03-19 114439](https://github.com/DEVADARSHAN2/Histogram-of-an-images/assets/119432150/bfae286b-f2de-400e-87b8-c53214a53936)
![Screenshot 2024-03-19 114446](https://github.com/DEVADARSHAN2/Histogram-of-an-images/assets/119432150/bcb11c54-2fff-4bb7-a109-0ebb44aa0558)


### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-19 114630](https://github.com/DEVADARSHAN2/Histogram-of-an-images/assets/119432150/3939ad94-b1ee-4526-8309-1171148eeb0b)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
