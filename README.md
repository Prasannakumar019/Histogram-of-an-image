# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:
Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
```python
# Developed By: M.Prasannakumar
# Register Number: 212220230035


# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('pras.jfif')
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
Color_image=cv2.imread('pras.jpg.jfif')
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
Gray_image=cv2.imread('pras.jfif',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```



## Output:
### Input Grayscale Image and Color Image
![11](https://user-images.githubusercontent.com/75235090/165019816-fdf5093f-147e-41fa-8e90-004f71b24d86.jpg)

![21](https://user-images.githubusercontent.com/75235090/165019823-4a8b5bdd-2e81-4a19-b111-d27b16048e48.jpg)


### Histogram of Grayscale Image and any channel of Color Image
![12](https://user-images.githubusercontent.com/75235090/165019853-fd7a2d76-5ce8-4be6-92f1-f81412f4f43a.jpg)

![22](https://user-images.githubusercontent.com/75235090/165019860-c34d4157-6eca-4fd6-a5e4-914f88d56049.jpg)

### Histogram Equalization of Grayscale Image
![pras 3](https://user-images.githubusercontent.com/75235090/165019875-020412d3-3858-4fb0-9ecc-ed1655fd20ee.jpg)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
