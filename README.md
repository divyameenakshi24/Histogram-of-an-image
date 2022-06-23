# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:
### Developed By: A.Divya Meenakshi
### Register Number: 212220230014
```python

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('j.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('ji.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('ji.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```



## Output:
### Input Grayscale Image and Color Image
![11](https://user-images.githubusercontent.com/75235402/164978192-923bddc4-275e-49e1-8700-cdd03828e24b.jpg)
![12](https://user-images.githubusercontent.com/75235402/164978196-f6a75f35-62f3-4757-9ae0-da5e53ee1f49.jpg)


### Histogram of Grayscale Image and any channel of Color Image
![21](https://user-images.githubusercontent.com/75235402/164978199-d54b9df7-3970-48e3-9cd2-dd66dbc7d7c9.jpg)

![22](https://user-images.githubusercontent.com/75235402/164978209-86daea20-6ff1-4cf3-b5a4-09c7bb0a11bc.jpg)


### Histogram Equalization of Grayscale Image
![3rd](https://user-images.githubusercontent.com/75235402/164978213-cacb356b-0755-4ed3-9d0e-2448faf6f27d.jpg)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
