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

```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("rome.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/9c67b669-bfaa-442b-ae47-66a84425985c)

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
![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/420e8962-a085-4586-8d09-fb695081c670)

![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/0f173b96-f289-4349-a29a-bf5ef5524ad8)

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
![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/e2568086-5fe1-4885-bf90-c7bfb2b2d82f)

![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/d69d21f8-75c3-4eac-b06b-768377fc61a6)

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
![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/40432992-a768-4d35-b9e7-7680c81dd1de)

![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/a3b544ef-589b-46ee-a02f-85d2a9e9c038)

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
![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/d4b9e4b5-20f7-4bfc-90f8-2074ac117c4f)

![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/4d536cf0-ab27-479f-8415-4edce04e0143)

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
![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/1b6ee790-147d-4839-9109-d555829753ee)

![image](https://github.com/Leann4468/EDGE-DETECTION/assets/121165979/2bef73c3-a3c4-45a4-889f-d06109ef8a29)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
