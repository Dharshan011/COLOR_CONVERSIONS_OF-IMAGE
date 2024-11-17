# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:
i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

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
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.
##### Program:
### Developed By: dharshan V
### Register Number: 212222230031
## Output:
### i)Read and Display an Image
```
import cv2
image=cv2.imread('msdd.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 160731](https://github.com/user-attachments/assets/8a21bca1-0cae-4c0d-99e7-9754e9d1b7d6)
<br>
### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
res = cv2.line(img, (0, 0), (300, 168), (200, 100, 300), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 161410](https://github.com/user-attachments/assets/d6771874-83e0-4002-a718-6c02d9d202a3)

ii)Draw a circle at the center of the image.
```
import cv2

# Load the image
img = cv2.imread("msdd.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 90, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![Screenshot 2024-09-09 161831](https://github.com/user-attachments/assets/8b4ca2a5-8db8-403d-bc50-42138fcdb8c4)

iii)Draw a rectangle around a specific region of interest in the image.
```
import cv2

img = cv2.imread("msdd.jpg")
start=(10,10)
stop=(200,150)
color=(100,255,100)
thickness=6
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![WhatsApp Image 2024-11-16 at 7 24 59 PM (1)](https://github.com/user-attachments/assets/d46cc55d-ed8e-4d66-b760-866de33b7c76)


iv)Add the text "MSD" at the top-left corner of the image.
```
import cv2

# Load the image
img = cv2.imread("msdd.jpg")

# Define the text to be added and its position
text = "MSD"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 162645](https://github.com/user-attachments/assets/df67fe3d-3157-426c-8b87-b4f653025bc8)
<br>
### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
import cv2
img = cv2.imread('msdd.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 162800](https://github.com/user-attachments/assets/1539482a-ab05-4d08-b767-22966bdcb125)

ii.)Convert the image from RGB to GRAY and display it.
```
import cv2
img = cv2.imread('msdd.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 163019](https://github.com/user-attachments/assets/047cf43f-e4ff-4cfa-8fdb-50a653841d11)

iii.)Convert the image from RGB to YCrCb and display it.
```
import cv2
img = cv2.imread('msdd.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 163113](https://github.com/user-attachments/assets/c26ffd9b-938c-4b7a-ae56-92ddfce1ddb6)

iv.)Convert the HSV image back to RGB and display it.
```
import cv2
img = cv2.imread('msdd.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 175059](https://github.com/user-attachments/assets/fa5a53e8-05e4-4228-85f5-2602257be409)
### iv)Access and Manipulate Image Pixels
```
import cv2

# Load and resize the image
img = cv2.imread('msdd.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 175115](https://github.com/user-attachments/assets/312eadc9-d379-4093-9764-529f98e86cbb)
### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 175923](https://github.com/user-attachments/assets/68225457-5953-4c26-8ccd-3c93f191eb6c)

### vi)Image Cropping
```
import cv2

# Load the image
image1=cv2.imread('msdd.jpg',1)

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 181535](https://github.com/user-attachments/assets/9321d335-8cbe-43a1-83f5-dcd99974a82b)

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
import cv2
img = cv2.imread("msdd.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 181548](https://github.com/user-attachments/assets/daea0375-26f2-45e2-842f-360eb96d35b7)

ii.)Flip the original image vertically and display it.
```
import cv2

img = cv2.imread("msdd.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 183224](https://github.com/user-attachments/assets/b66ec7b6-df97-401b-bcbf-d67c44f8add0)
![Screenshot 2024-09-09 181716](https://github.com/user-attachments/assets/22c38b66-09f3-4019-bedb-a6489f3e008e)


<br>
<br>

### viii)Write and Save the Modified Image
```
 cv2.imwrite('lion.jpg',image)
```
![Screenshot 2024-09-09 181821](https://github.com/user-attachments/assets/e1dbbd26-d5db-4f15-9c2f-422e9e7bbeb0)
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.














