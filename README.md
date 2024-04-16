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
## code
```
import cv2
# Read the image
image = cv2.imread('username.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Gaussian blur
img_blurred = cv2.GaussianBlur(gray_image, (3, 3), 0)

# Sobel edge detection
sobelx = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 0, ksize=5)
sobely = cv2.Sobel(img_blurred, cv2.CV_64F, 0, 1, ksize=5)
sobelxy = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 1, ksize=5)

# Laplacian edge detection
laplacian = cv2.Laplacian(img_blurred, cv2.CV_64F)

# Canny edge detection
canny_edges = cv2.Canny(img_blurred, 120, 150)

# Display images
cv2.imshow('Original', gray_image)
cv2.imshow('Sobel X', sobelx)
cv2.imshow('Sobel Y', sobely)
cv2.imshow('Sobel XY', sobelxy)
cv2.imshow('Laplacian', laplacian)
cv2.imshow('Canny Edges', canny_edges)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### SOBEL EDGE DETECTOR

![Screenshot 2024-04-15 171625](https://github.com/Hariveeraprasad-2006/EDGE-DETECTION/assets/145049988/ca39255b-c065-4d6e-ac1f-eeed3666b0df)
![Screenshot 2024-04-15 171651](https://github.com/Hariveeraprasad-2006/EDGE-DETECTION/assets/145049988/7344028b-ea8c-43b0-b96e-d66271cdcdee)
![Screenshot 2024-04-15 171713](https://github.com/Hariveeraprasad-2006/EDGE-DETECTION/assets/145049988/281de6de-4073-484a-9ecd-a9d60b9f8fd6)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-04-15 171732](https://github.com/Hariveeraprasad-2006/EDGE-DETECTION/assets/145049988/bedfb74b-d3fb-4b77-be44-45796e53481c)



### CANNY EDGE DETECTOR
![Screenshot 2024-04-15 171801](https://github.com/Hariveeraprasad-2006/EDGE-DETECTION/assets/145049988/dac173f1-d1d5-40a9-b93d-e8587096aaef)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
