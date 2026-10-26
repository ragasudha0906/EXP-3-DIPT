# EX 03 - RECORD-HISTOGRAM PROCESSING
## NAME : RAGASUDHA R
## REG NO :212224230215
## CODE
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
img = cv2.imread('photo.jpeg', cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()
plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()
img_eq = cv2.equalizeHist(img)
plt.hist(img_eq.ravel(), 256, range = [0, 256])
plt.title('Equalized Histogram')
plt.imshow(img_eq, cmap='gray')
plt.title('Original Image')
plt.show()
img = cv2.imread('photo.jpeg', cv2.IMREAD_COLOR)
img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])
img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
 plt.imshow(img_eq[:,:,::-1]); plt.title('Equalized Image');plt.show()
plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()
plt.figure(figsize = (20,10))
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.show()
plt.figure(figsize = [15,4])
plt.subplot(121); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(122); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')
```
## OUTPUT
<img width="980" height="542" alt="image" src="https://github.com/user-attachments/assets/620f9336-4b6c-4555-9e16-db4521c72bba" />
<img width="1032" height="541" alt="image" src="https://github.com/user-attachments/assets/901b670f-9bf3-463f-85bc-066a96eeea97" />
<img width="1062" height="582" alt="image" src="https://github.com/user-attachments/assets/11460484-a474-48da-9d8e-69e2d5b2e4ec" />
<img width="1007" height="566" alt="image" src="https://github.com/user-attachments/assets/28820d64-d233-493d-97c0-e9f63d0aa464" />
<img width="947" height="551" alt="image" src="https://github.com/user-attachments/assets/6e88a81c-4d49-4740-b0d6-fa616a4af6a7" />
<img width="1026" height="556" alt="image" src="https://github.com/user-attachments/assets/ee8997be-ae1c-4b9e-acfe-30a9dc937807" />
<img width="1245" height="431" alt="image" src="https://github.com/user-attachments/assets/54151227-78fa-4fca-b16a-272a67d73997" />
<img width="1251" height="415" alt="image" src="https://github.com/user-attachments/assets/d3bc373f-ee58-4798-96f3-3342ff34378c" />
## RESULT



