# Image Smoothing and Sharpening Using OpenCV

## Aim

To write a Python program using OpenCV to apply different smoothing filters (Averaging, Weighted Averaging, Gaussian, Median) and sharpening filters (Laplacian Kernel and Laplacian Operator) for image enhancement, and display each result separately along with the original image for comparison.

---

## The program performs the following operations:

- Read and display an input image  
- Apply Averaging filter  
- Apply Weighted Averaging filter  
- Apply Gaussian filter  
- Apply Median filter  
- Apply Laplacian sharpening using kernel  
- Apply Laplacian operator  
- Display all outputs for comparison  

---

##  Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

##  Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the input image (e.g., `image.jpg`).

### Step 3:
Convert the image from BGR to RGB format for display.

### Step 4:
Apply Averaging Filter using `cv2.blur()`.

### Step 5:
Apply Weighted Averaging Filter using a custom kernel with `cv2.filter2D()`.

### Step 6:
Apply Gaussian Filter using `cv2.GaussianBlur()`.

### Step 7:
Apply Median Filter using `cv2.medianBlur()`.

### Step 8:
Apply Laplacian Sharpening using Kernel with `cv2.filter2D()`.

### Step 9:
Convert image to grayscale and apply Laplacian Operator using `cv2.Laplacian()`.

### Step 10:
Display all filtered images using a grid layout for comparison.

---

##  Developed By

- **Name:** JANAGIRAMAN M
- **Register No:** 212224230101 

---

## PROGRAM :
```python

import cv2
import matplotlib.pyplot as plt
import numpy as np

image1 = cv2.imread('mountain view.jpeg')
if image1 is None:
    raise FileNotFoundError("red.jpg was not found. Place red.jpg in the same folder as this notebook.")

image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
kernel = np.ones((5, 5), np.float32) / 25
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image3)
plt.title('Averaging Filter Image')
plt.axis('off')
plt.show()
```

```python
# In[2]: Using Weighted Averaging Filter

kernel1 = np.array([[1, 2, 1],
                    [2, 4, 2],
                    [1, 2, 1]], dtype=np.float32) / 16

weighted_image = cv2.filter2D(image2, -1, kernel1)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(weighted_image)
plt.title('Weighted Average Filter Image')
plt.axis('off')
plt.show()
```

```python
# In[3]: Using Gaussian Filter

gaussian_blur = cv2.GaussianBlur(image2, (5, 5), 0)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(gaussian_blur)
plt.title('Gaussian Blur')
plt.axis('off')
plt.show()
```

```python
# In[4]: Using Median Filter

median = cv2.medianBlur(image2, 5)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(median)
plt.title('Median Filter Image')
plt.axis('off')
plt.show()
```

```python
# In[5]: Using Laplacian Kernel

kernel2 = np.array([[0, -1, 0],
                    [-1, 5, -1],
                    [0, -1, 0]], dtype=np.float32)

sharpened_image = cv2.filter2D(image2, -1, kernel2)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(sharpened_image)
plt.title('Sharpened Image - Laplacian Kernel')
plt.axis('off')
plt.show()
```

```python
# In[6]: Using Laplacian Operator

gray = cv2.cvtColor(image1, cv2.COLOR_BGR2GRAY)
laplacian = cv2.Laplacian(gray, cv2.CV_64F)
laplacian_abs = cv2.convertScaleAbs(laplacian)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(image2)
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(laplacian_abs, cmap='gray')
plt.title('Laplacian Operator')
plt.axis('off')
plt.show()
```

##  Output

### Smoothing Filters

- Averaging filter produces blurred image

<img width="712" height="500" alt="image" src="https://github.com/user-attachments/assets/15a40651-48ab-424a-b909-17a78c2ffc5f" />

- Weighted averaging provides smoother result with less distortion

<img width="718" height="491" alt="image" src="https://github.com/user-attachments/assets/9b5b81f5-bdec-4d59-896a-ddc1e0ba8337" />

- Gaussian filter preserves edges better while reducing noise

<img width="725" height="491" alt="image" src="https://github.com/user-attachments/assets/a7d65f77-1fa2-495d-bf8f-744d0d07fdb1" />

- Median filter removes salt-and-pepper noise effectively

<img width="727" height="482" alt="image" src="https://github.com/user-attachments/assets/eabe8198-c663-4264-9211-c7e874762ff1" />


###  Sharpening Filters

- Laplacian kernel enhances edges and fine details

<img width="722" height="490" alt="image" src="https://github.com/user-attachments/assets/cbf2ba5e-2647-4197-ba69-c77aa993b23a" />

- Laplacian operator detects edges clearly in grayscale

<img width="730" height="492" alt="image" src="https://github.com/user-attachments/assets/cbcc0ab8-a48b-402f-beb9-233b00715c3d" />


---

##  Result

Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.

The smoothing filters reduce noise and improve image quality, while sharpening filters enhance edges and details for better feature extraction.
