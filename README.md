# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]]) translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]]) reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### tep6:
Rotate the image using angle=np.radians(45) M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]]) rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step7:
Crop the image using cropped_img=input_img[20:150,60:230]

### Step8:
Display all the Transformed images and end the program.

## Program:
```python
Developed By: M Gautham
Register Number: 212221230027
```
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
inputImage=cv2.imread("cat.jpg")
inputImage=cv2.cvtColor(inputImage, cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(inputImage)
plt.show()
rows, cols, dim = inputImage.shape
M= np.float32([[1, 0, 100],
                [0, 1, 200],
                 [0, 0, 1]])
translatedImage =cv2.warpPerspective (inputImage, M, (cols, rows))
plt.imshow(translatedImage)
plt.show()
```

ii) Image Scaling
```
rows, cols, dim = inputImage.shape
M = np. float32 ([[1.5, 0 ,0],
                 [0, 1.8, 0],
                  [0, 0, 1]])
scaledImage=cv2.warpPerspective(inputImage, M, (cols * 2, rows * 2))
plt.imshow(scaledImage)
plt.show()
```
iii)Image shearing
```
matrixX = np.float32([[1, 0.5, 0],
                      [0, 1 ,0],
                      [0, 0, 1]])

matrixY = np.float32([[1, 0, 0],
                      [0.5, 1, 0],
                      [0, 0, 1]])
shearedXaxis = cv2.warpPerspective (inputImage, matrixX, (int(cols * 1.5), int (rows * 1.5)))
shearedYaxis = cv2.warpPerspective (inputImage, matrixY, (int (cols * 1.5), int (rows * 1.5)))
plt.imshow(shearedXaxis)
plt.show()
plt.imshow(shearedYaxis)
plt.show()
```
iv)Image Reflection
```
matrixx=np.float32([[1, 0, 0],
                    [0,-1,rows],
                    [0,0,1]])
matrixy=np.float32([[-1, 0, cols],
                    [0,1,0],
                    [0,0,1]])
reflectedX=cv2.warpPerspective(inputImage, matrixx, (cols, rows))
reflectedY=cv2.warpPerspective(inputImage, matrixy, (cols, rows))
plt.imshow(reflectedY)
plt.show()
```
v)Image Rotation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
angle=np.radians(45)
inputImage=cv2.imread("cat.jpg")
rows, cols, dim = inputImage.shape
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotatedImage = cv2.warpPerspective(inputImage,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotatedImage)
plt.show()
```
vi)Image Cropping
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
angle=np.radians(45)
inputImage=cv2.imread("cat.jpg")
CroppedImage= inputImage[20:150, 60:230]
plt.axis('off')
plt.imshow(CroppedImage)
plt.show()
```
## Output:
### i)Image Translation
![image](https://github.com/muppirgautham/IMAGE-TRANSFORMATIONS/assets/94810884/a389c721-0189-41ff-8d77-4d43963ace9f)


### ii) Image Scaling
![image](https://github.com/muppirgautham/IMAGE-TRANSFORMATIONS/assets/94810884/53512234-344e-4b6a-9e34-c08fc0f9579f)



### iii)Image shearing
![image](https://github.com/muppirgautham/IMAGE-TRANSFORMATIONS/assets/94810884/3312a335-693d-4c02-bb67-d42140b9779a)


### iv)Image Reflection
![image](https://github.com/muppirgautham/IMAGE-TRANSFORMATIONS/assets/94810884/12b130ae-a2b7-4333-9a29-69fefb47dcc0)




### v)Image Rotation
![image](https://github.com/muppirgautham/IMAGE-TRANSFORMATIONS/assets/94810884/8302d075-f49b-456d-aecb-87b7289d01a6)



### vi)Image Cropping
![image](https://github.com/muppirgautham/IMAGE-TRANSFORMATIONS/assets/94810884/6a24d480-1774-46a6-a0e6-66ce7e12ecb8)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
