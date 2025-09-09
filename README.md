# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import all the necessary modules

### Step2:
<br>
Choose an image and save it as filename.jpg

### Step3:
<br>
Use imread to read the image

### Step4:
<br>
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
<br>
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:
Crop the image to remove unwanted areas from an image

### Step10:
Use cv2.imshow to show the image

### Step11:
End the program

## Program:

Developed By: SAI HRISHI M

Register Number: 212224240140

i)Image Translation

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Pictures\Screenshots\Regular Screenshots\Screenshot 2025-05-23 213919.png")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],[0,1,50],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()

```

ii) Image Scaling

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Pictures\Screenshots\Regular Screenshots\Screenshot 2025-05-23 213919.png")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()

```


iii)Image Shearing

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Pictures\Screenshots\Regular Screenshots\Screenshot 2025-05-23 213919.png")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()

```



iv)Image Reflection

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Pictures\Screenshots\Regular Screenshots\Screenshot 2025-05-23 213919.png")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()

```



v)Image Rotation

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread(r"C:\Users\admin\Pictures\Screenshots\Regular Screenshots\Screenshot 2025-05-23 213919.png")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Rotation:")
plt.imshow(translated_image)
plt.show()

```



vi)Image Cropping

```python

import cv2
import matplotlib.pyplot as plt
image = cv2.imread(r"C:\Users\admin\Pictures\Screenshots\Regular Screenshots\Screenshot 2025-05-23 213919.png")
h, w, _ = image.shape
cropped_face = image[int(h*0.2):int(h*0.8), int(w*0.3):int(w*0.7)]
cv2.imwrite("cropped_pigeon_face.jpg", cropped_face)
plt.imshow(cv2.cvtColor(cropped_face, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```

### Output:
### i)Image Translation

<img width="623" height="510" alt="Screenshot 2025-09-10 023311" src="https://github.com/user-attachments/assets/bbec6135-16b2-4a96-a091-07ff84ae5008" />

### ii) Image Scaling

<img width="623" height="523" alt="Screenshot 2025-09-10 023319" src="https://github.com/user-attachments/assets/2c418403-8380-4360-a0f6-527cd0d8c198" />

### iii)Image shearing

<img width="613" height="522" alt="Screenshot 2025-09-10 023328" src="https://github.com/user-attachments/assets/a2215785-026f-4970-a8d0-2cd3fd00fd00" />

### iv)Image Reflection


<img width="619" height="519" alt="Screenshot 2025-09-10 023338" src="https://github.com/user-attachments/assets/55a71b03-0353-4759-bd15-5d1713ca6383" />


### v)Image Rotation


<img width="613" height="512" alt="Screenshot 2025-09-10 023839" src="https://github.com/user-attachments/assets/2ee41408-ee4c-4869-bbb8-dc56506dfe94" />


### vi)Image Cropping


<img width="418" height="492" alt="Screenshot 2025-09-10 023347" src="https://github.com/user-attachments/assets/7a8bac79-265c-4648-a7e3-4ffa008800c4" />


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
