# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 library and upload the image or capture an image.
<br>
### Step2:
Read the saved image using cv2.imread("filename.jpg").
<br>

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.
<br>

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])
<br>

### Step5:
Output the image using cv2.imshow("OUTPUT", image)
<br>

## Program:
```python
# Developed By: Harshini M
# Register Number: 212220230022
# i) Convert BGR and RGB to HSV and GRAY

import cv2
img = cv2.imread("image.jpg")
cv2.imshow("Original Image",img)
cv2.waitKey(0)
cv2.destroyAllWindows()

hsv_image=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR2HSV",hsv_image)

gray_image=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR2Gray",gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

hsv_image1=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB2HSV",hsv_image1)

gray_image1=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB2Gray",gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

bgr_image=cv2.cvtColor(hsv_image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV2BGR",bgr_image)

rgb_image=cv2.cvtColor(hsv_image1,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB",rgb_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

YCrCb_image=cv2.cvtColor(bgr_image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR2YCrCb",YCrCb_image)

YCrCb_image1=cv2.cvtColor(rgb_image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB2YCrCb",YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()


# iv)Split and Merge RGB Image

blue = rgb_image[:,:,0]
green = rgb_image[:,:,1]
red = rgb_image[:,:,2]
cv2.imshow("r plane",red)
cv2.imshow("g plane",green)
cv2.imshow("b plane",blue)
m=cv2.merge((blue,green,red))
cv2.imshow("merged",m)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

h, s, v = cv2.split(hsv_image)
cv2.imshow("h plane",h)
cv2.imshow("s plane",s)
cv2.imshow("v plane",v)
merged = cv2.merge((h,s,v))
cv2.imshow("merge",merged)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<img width="445" alt="image" src="https://user-images.githubusercontent.com/75235554/162723762-21afc9dc-e121-48ad-98a3-e1c83996f629.png">


<img width="423" alt="image" src="https://user-images.githubusercontent.com/75235554/162723915-c1719797-df80-4600-8bd3-ab7806d55d24.png">


<br>

### ii) HSV to RGB and BGR
<br>
<img width="414" alt="image" src="https://user-images.githubusercontent.com/75235554/162724067-12efba6b-0aec-4472-ab35-cf941c07662c.png">
<br>

### iii) RGB and BGR to YCrCb
<br>
<img width="399" alt="image" src="https://user-images.githubusercontent.com/75235554/162724237-fae71c27-8166-4a96-ac86-0b32dff0ac66.png">
<br>

### iv) Split and merge RGB Image
<br>
<img width="431" alt="image" src="https://user-images.githubusercontent.com/75235554/162724483-aa16ba9d-3e4c-4e8f-804a-fbcc76e849cd.png">
<br>

### v) Split and merge HSV Image
<br>
<img width="416" alt="image" src="https://user-images.githubusercontent.com/75235554/162724621-12c54829-3b16-4dbf-910e-eb1f44ade156.png">
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
