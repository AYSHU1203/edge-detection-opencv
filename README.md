# edge-detection-opencv
# Name:AYSHWARIYA J
# Reg no:212224230030

## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Sobel operator** using OpenCV to detect edges.

### Step 5:
Apply **Prewitt operator** using custom kernels.

### Step 6:
Apply **Roberts operator** using custom kernels.

### Step 7:
Apply **Laplacian operator** using OpenCV.

### Step 8:
Apply **Canny edge detector** using OpenCV.

### Step 9:
Display all edge-detected images for comparison.

---

## Developed By

  ## Name: Ayshwariya J
  ### Register No: 212224230030

---

## Output
## Original Image:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Qno.1.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## OUTPUT:
<img width="621" height="627" alt="image" src="https://github.com/user-attachments/assets/d6b2a953-062e-4a97-8342-e7a602014eff" />




### Sobel Edge Detector:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## OUTPUT:
<img width="602" height="625" alt="image" src="https://github.com/user-attachments/assets/1acdab28-b788-4f7d-b689-5460a9100b0e" />


### Laplacian Edge Detector:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## OUTPUT:
<img width="598" height="600" alt="image" src="https://github.com/user-attachments/assets/834e831d-07fb-4e0e-8cfe-307b7a9ed6f9" />




### Canny Edge Detector:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## OUTPUT:
<img width="607" height="617" alt="image" src="https://github.com/user-attachments/assets/fa2cc00a-efb8-42ec-9885-02b11031f856" />


## Result

Thus, edges are successfully detected using Sobel, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
