# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
## NAME: LAAKSHIT D
## REG.NO: 212222230071
```
### Convert image to grayscale and remove noise

```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dip 6 .png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## Sobel edge detection:
### Sobel x axis:

```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
Sobel y axis:

```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
###Sobel xy axis:

```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

### LAPLACIAN EDGE DETECTOR:

```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR:

```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
## SOBEL EDGE DETECTOR
### Sobel x axis:

![6 dip 1](https://github.com/KRISHNARAJ-D/EDGE-DETECTION/assets/119559695/d8e1751f-1a34-4cbb-a6df-93e9351980ef)

### Sobel y axis:

![6 dip 2](https://github.com/KRISHNARAJ-D/EDGE-DETECTION/assets/119559695/bbb22409-3a88-461e-8202-52280dab0cd5)

### Sobel xy axis:

![6 dip 3](https://github.com/KRISHNARAJ-D/EDGE-DETECTION/assets/119559695/b2df63cb-f0ea-44de-a284-2e8cdc706dc2)


### LAPLACIAN EDGE DETECTOR:

![6 dip 4](https://github.com/KRISHNARAJ-D/EDGE-DETECTION/assets/119559695/74b1852a-34a0-4deb-bcbc-c20d1a8e7630)

### CANNY EDGE DETECTOR:
![6 dip 5](https://github.com/KRISHNARAJ-D/EDGE-DETECTION/assets/119559695/e8516b07-bd94-4f7a-af90-95a43363fc89)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
