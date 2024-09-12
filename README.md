# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By: DHARSHAN V
### Register Number: 212222230031


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
import cv2
image=cv2.imread('dog.png',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('NATUREK',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 152357](https://github.com/user-attachments/assets/bcebfcf9-a059-4d77-a533-4ad9913ba877)


### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("dog.png")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 152537](https://github.com/user-attachments/assets/974de23a-81b2-4676-8de7-d026f3bfd83e)


2. Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("dog.png")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 152636](https://github.com/user-attachments/assets/7a4fffd4-e9cf-425e-85bc-27a0800ad475)


3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("dog.png")
image = cv2.resize(image, (400, 300))
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-12 152706](https://github.com/user-attachments/assets/8218cf6a-26cb-46eb-a930-5fbc384ccc2a)


4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("dog.png")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 152733](https://github.com/user-attachments/assets/fcf6a393-69c5-465d-b159-e9aaf7010207)


### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('dog.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 152803](https://github.com/user-attachments/assets/64b6a9f0-1c33-4288-88d7-b9656d46cdad)


(2) Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('dog.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-12 152848](https://github.com/user-attachments/assets/d618eff4-75d1-4127-818c-709cd46c09b2)


(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('dog.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-12 152914](https://github.com/user-attachments/assets/b3fae7e3-2ecd-4309-b686-9613d4406ad0)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('dog.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 152944](https://github.com/user-attachments/assets/48c64e93-1649-4091-b3cd-5767ae89d683)



### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```

![Screenshot 2024-09-12 153251](https://github.com/user-attachments/assets/7c98c95f-9def-488a-942c-38a4998ae012)


(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('dog.png',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-12 153027](https://github.com/user-attachments/assets/c4cd48be-c93f-4640-a01d-b85009278fa1)


### v)Image Resizing:
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 153052](https://github.com/user-attachments/assets/38f22138-acb1-4093-83f7-b3fa3f253292)



### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('dog.png',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 153117](https://github.com/user-attachments/assets/72b32d55-a45c-491e-8a32-5a647a8bfdf4)


### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("dog.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-12 153142](https://github.com/user-attachments/assets/0c59aaa8-26f9-43e9-94c8-368c7fde5163)



(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("dog.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-12 153205](https://github.com/user-attachments/assets/344e1c04-a11d-49f9-82b6-1c6956369ce4)


### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("dog.png")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
![Screenshot 2024-09-12 153237](https://github.com/user-attachments/assets/3ebd47d5-f3cc-4b36-99ca-17155774b799)

## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.






