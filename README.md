# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
</br> 

### Step2
</br>
</br> 

### Step3
</br>
</br> 

### Step4
</br>
</br> 

### Step5
</br>
</br> 

## Program:
### Developed By   : K KESAVA SAI
### Register Number: 212223230105
</br>

### 1. Smoothing Filters

## i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("earth1.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal = np.ones((11,11),np.float32)/121
img2 = cv2.filter2D(img1,-1,kernal)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')
```
## ii) Using Weighted Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("earth1.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
img2 = cv2.filter2D(img1,-1,kernal2)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')



```
## iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("earth1.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur =  cv2.GaussianBlur(src=img1,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title('Filtered')
plt.axis('off')

```

iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("earth1.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=img1,ksize=11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(median)
plt.title('Filtered')
plt.axis('off')



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("earth1.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img3)
plt.title('Filtered')
plt.axis('off')



```
ii) Using Laplacian Operator
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("earth1.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)
new_img = cv2.Laplacian(img1,cv2.CV_64F)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(new_img)
plt.title('Filtered')
plt.axis('off')
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![image](https://github.com/Kesavasai20/Implementation-of-filter/assets/138849303/7359c071-4a2e-48c6-af7f-27f86235f5d6)

ii) Using Weighted Averaging Filter
![image](https://github.com/Kesavasai20/Implementation-of-filter/assets/138849303/8c49fec7-0675-4900-afa6-9e501561f04b)

iii) Using Gaussian Filter
![image](https://github.com/Kesavasai20/Implementation-of-filter/assets/138849303/a0d25d0c-360a-4022-858f-a9f3de77482a)

iv) Using Median Filter
![image](https://github.com/Kesavasai20/Implementation-of-filter/assets/138849303/85403d50-8008-4d56-87f8-fa101392fefb)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![image](https://github.com/Kesavasai20/Implementation-of-filter/assets/138849303/ff939e40-d019-4f68-9ca2-e36e18811ace)

ii) Using Laplacian Operator
![image](https://github.com/Kesavasai20/Implementation-of-filter/assets/138849303/4bae56a8-41be-45b8-ad82-57983023dfaa)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
