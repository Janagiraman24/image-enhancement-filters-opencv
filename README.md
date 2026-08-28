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
