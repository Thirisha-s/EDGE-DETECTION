# Ex 06 EDGE-DETECTION
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

## Output:
```
NAME: S.Thirisha
REGISTER NUMBER: 212222230160
```

```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("light.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
![image](https://github.com/Thirisha-s/EDGE-DETECTION/assets/120380280/ff55227f-6613-4fe8-832b-dac8762f3465)


### SOBEL EDGE DETECTOR

## SOBEL X AXIS
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
![image](https://github.com/Thirisha-s/EDGE-DETECTION/assets/120380280/27892053-ce84-4cb0-b173-0d71b3bc8e5c)


## SOBEL Y AXIS
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
![image](https://github.com/Thirisha-s/EDGE-DETECTION/assets/120380280/42ec975f-a463-4850-afec-719f822513b0)


## SOBEL XY AXIS
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
![image](https://github.com/Thirisha-s/EDGE-DETECTION/assets/120380280/f34b4830-70b4-4248-a9f8-d0a94c9cc58b)


### LAPLACIAN EDGE DETECTOR
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
![image](https://github.com/Thirisha-s/EDGE-DETECTION/assets/120380280/e6271081-a480-4794-9433-73f3a0de5a18)

### CANNY EDGE DETECTOR
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
![Screenshot 2024-04-22 183217](https://github.com/Thirisha-s/EDGE-DETECTION/assets/120380280/413d3a7c-0532-4d10-bd98-bea101931f5c)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
