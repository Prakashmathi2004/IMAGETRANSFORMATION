# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
Write a code to translation of the image.

### Step3:
Write a code for scaling of the image.

### Step4:
Write a code for shearing of the image.

### Step5:
Write a code for reflection of the image.

### Step6:
Display all the Transformed images.

## Program:

Developed By:PRAKASH M
Register Number: 212222100035

i)Image Translation
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
~~~

ii) Image Scaling
~~~
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv
rows,cols,dim = image.shape

M_scale = np.float32([[1,0,0], [0,1.5,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.axis("off")
plt.imshow(scale_image)
plt.show()
~~~

iii)Image shearing
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("m.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
~~~

iv)Image Reflection
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("m.jpg")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
~~~


v)Image Rotation
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
~~~

vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

<img width="281" alt="image" src="https://github.com/Prakashmathi2004/IMAGETRANSFORMATION/assets/118350045/7beeaa0c-3c64-4f30-876e-8c32d78f29ca">

### ii) Image Scaling

<img width="280" alt="image" src="https://github.com/Prakashmathi2004/IMAGETRANSFORMATION/assets/118350045/487dbacf-9a7b-4d17-bdca-81f23003223f">

### iii)Image shearing
<img width="284" alt="image" src="https://github.com/Prakashmathi2004/IMAGETRANSFORMATION/assets/118350045/ace73fe3-6644-470c-82b3-57057f72b1c7">

### iv)Image Reflection
<img width="186" alt="image" src="https://github.com/Prakashmathi2004/IMAGETRANSFORMATION/assets/118350045/2535c426-3bf1-4838-a567-8d5291633805">

### v)Image Rotation
<img width="279" alt="image" src="https://github.com/Prakashmathi2004/IMAGETRANSFORMATION/assets/118350045/635b1b8e-2386-4225-ba5b-65a2294ff7e1">

### vi)Image Cropping
<img width="253" alt="image" src="https://github.com/Prakashmathi2004/IMAGETRANSFORMATION/assets/118350045/f921516c-e8bf-4f0d-8186-11983f7c73a5">


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
