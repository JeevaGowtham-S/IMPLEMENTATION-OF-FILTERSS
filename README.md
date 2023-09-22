# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1\
Import the required modules.
</br>
</br> 

### Step2
Convert the image from BGR to RGB.

</br>
</br> 

### Step3
Apply the required filters for the image separately.
</br>
</br> 

### Step4
Plot the original and filtered image by using matplotlib.pyplot
</br>
</br> 

### Step5
End the program.
</br>
</br> 

## Program:
### Developed By:  JEEVAGOWTHAM S
### Register Number: 212222230053
</br>

### 1. Smoothing Filters:
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("cat.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
i) Using Averaging Filter
```Python
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




```
ii) Using Weighted Averaging Filter
```Python

kernel2=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(33,33),sigmaX=0,sigmaY=0)
plt.figure(figsize=(9,9))
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

iv) Using Median Filter
```Python
median=cv2.medianBlur(src=image2,ksize=11)
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

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel3=np.array([[0,-1,-1],[2,-4,1],[2,1,0]])
image3=cv2.filter2D(image2,-1,kernel3)
plt.figure(figsize=(9,9))
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
ii) Using Laplacian Operator
```Python
new_image=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(new_image)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter:

![Screenshot 2023-09-09 160623](https://github.com/JeevaGowtham-S/IMPLEMENTATION-OF-FILTERSS/assets/118042624/605193ae-d749-4762-843e-51190fff37b1)

</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter:

![Screenshot 2023-09-09 160924](https://github.com/JeevaGowtham-S/IMPLEMENTATION-OF-FILTERSS/assets/118042624/ce5c4ffb-0b0a-418a-8639-20ef22b423d0)


</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter:

![Screenshot 2023-09-09 161303](https://github.com/JeevaGowtham-S/IMPLEMENTATION-OF-FILTERSS/assets/118042624/6e0d24b4-5b17-4236-bac3-19451daa461b)


</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter:

![Screenshot 2023-09-09 161357](https://github.com/JeevaGowtham-S/IMPLEMENTATION-OF-FILTERSS/assets/118042624/3e86c2f5-9ebc-437d-a460-5dc67c9a2c7e)



</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal:

![Screenshot 2023-09-09 162046](https://github.com/JeevaGowtham-S/IMPLEMENTATION-OF-FILTERSS/assets/118042624/660d2654-8a7c-4224-801b-2dc40c5eef8f)


</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator:

![Screenshot 2023-09-09 162153](https://github.com/JeevaGowtham-S/IMPLEMENTATION-OF-FILTERSS/assets/118042624/39697256-dd0a-4c81-a4c1-faa91d4583ea)


</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
