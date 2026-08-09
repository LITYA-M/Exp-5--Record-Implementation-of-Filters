# Exp-5--Record-Implementation-of-Filters
Aim
To write a Python program using OpenCV to apply different smoothing filters (Averaging, Weighted Averaging, Gaussian, Median) and sharpening filters (Laplacian Kernel and Laplacian Operator) for image enhancement, and display each result separately along with the original image for comparison.

The program performs the following operations:
Read and display an input image
Apply Averaging filter
Apply Weighted Averaging filter
Apply Gaussian filter
Apply Median filter
Apply Laplacian sharpening using kernel
Apply Laplacian operator
Display all outputs for comparison
Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
Algorithm
Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:
Read the input image (e.g., image.jpg).

Step 3:
Convert the image from BGR to RGB format for display.

Step 4:
Apply Averaging Filter using cv2.blur().

Step 5:
Apply Weighted Averaging Filter using a custom kernel with cv2.filter2D().

Step 6:
Apply Gaussian Filter using cv2.GaussianBlur().

Step 7:
Apply Median Filter using cv2.medianBlur().

Step 8:
Apply Laplacian Sharpening using Kernel with cv2.filter2D().

Step 9:
Convert image to grayscale and apply Laplacian Operator using cv2.Laplacian().

Step 10:
Display all filtered images using a grid layout for comparison.

## Program
### Ex.No:5 Implementation of filter
### Name: LITYA M
### Register No: 212225230152

1.Averaging filter produces blurred image

```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("litya .jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```

2.Weighted averaging provides smoother result with less distortion

```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

3.Gaussian filter preserves edges better while reducing noise

```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
4.Median filter removes salt-and-pepper noise effectively
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

5.Laplacian kernel enhances edges and fine details

```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

6.Laplacian operator detects edges clearly in grayscale

```
laplacian = cv2.Laplacian(image2, cv2.CV_64F)

plt.subplot(1,2,1)
plt.imshow(cv2.cvtColor(image2, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")

plt.show()
```

## output

1.Smoothing Filters
1.Averaging filter produces blurred image

<img width="897" height="800" alt="image" src="https://github.com/user-attachments/assets/0b06f046-678a-45b7-b656-9bde56f361ec" />

2.Weighted averaging provides smoother result with less distortion

<img width="632" height="512" alt="image" src="https://github.com/user-attachments/assets/5651987c-6e38-426c-b871-d6d664a88ecb" />

3.Gaussian filter preserves edges better while reducing noise

<img width="567" height="505" alt="image" src="https://github.com/user-attachments/assets/6243af56-1697-4330-8171-af51136bf00b" />

4.Median filter removes salt-and-pepper noise effectively

<img width="877" height="786" alt="image" src="https://github.com/user-attachments/assets/eba96765-d932-41c4-933a-8793e9d54e0b" />

2.Sharpening Filters
1.Laplacian kernel enhances edges and fine details

<img width="601" height="520" alt="image" src="https://github.com/user-attachments/assets/d86ca5b9-26b5-49f1-a3d6-088dd697b04e" />

2.Laplacian operator detects edges clearly in grayscale

<img width="582" height="512" alt="image" src="https://github.com/user-attachments/assets/9b4e3726-23d6-4cd6-b8f6-b710ee2eeb33" />

## Result

Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.

The smoothing filters reduce noise and improve image quality, while sharpening filters enhance edges and details for better feature extraction.

..











..














..





















..











..












..
















..



















..

















..


























..


















..






















..















..
















..

















..













..


















..











..
















...










..














...










...
















...





















..
