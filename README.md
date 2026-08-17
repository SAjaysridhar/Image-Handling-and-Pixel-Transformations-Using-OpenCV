# EXP-1 Image-Handling-and-Pixel-Transformations-Using-OpenCV

# Program Developed By

**Name:** AJAY S

**Register Number:** 212224230010


## AIM
Write a Python program using OpenCV to perform basic image processing operations including:

- Read and display an image.
- Draw basic shapes and text.
- Perform color space conversions.
- Access and modify pixel values.
- Resize and crop an image.
- Flip an image horizontally and vertically.

---

## Software Required
- Anaconda (Python 3.7 or above)
- Jupyter Notebook
- OpenCV (`cv2`)
- Matplotlib

---

## Algorithm

### Step 1
Import the required libraries (`cv2`, `matplotlib.pyplot`).

### Step 2
Read the image from the local directory and display it.

### Step 3
Draw graphical objects such as:
- Line
- Circle
- Rectangle
- Text

### Step 4
Convert the image into different color spaces:
- RGB
- HSV
- Grayscale
- YCrCb

### Step 5
Modify pixel values by changing a selected region.

### Step 6
Resize the image.

### Step 7
Crop a Region of Interest (ROI).

### Step 8
Flip the image horizontally and vertically.

---

# Ex. No. 01

## 1. Import the required libraries.

```python
import cv2
import matplotlib.pyplot as plt
```

---

## 2. Read the image.

```python
img = cv2.imread('img 1.jpg', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

## 3. Display the image.

```python
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('on')  # Removes axis ticks and labels
plt.show()
```

### Output

<img width="966" height="533" alt="image" src="https://github.com/user-attachments/assets/e9a46374-e581-411f-9dee-c223c8868d76" />



---

## 4. Draw a diagonal line.

```python
image = cv2.imread('img 1.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (0, 0, 255), 2)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('on')  
plt.show()
```

### Output

<img width="887" height="543" alt="image" src="https://github.com/user-attachments/assets/9b850584-17fd-40fd-be4e-8f1b48f8311e" />



---

## 5. Draw a circle.

```python
circle_img = cv2.circle(img_rgb,(200,150),15,(255,0,0),10)

plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('on')  
plt.show()
```

### Output
<img width="830" height="530" alt="image" src="https://github.com/user-attachments/assets/b31d37c7-2120-4a4a-9e41-a8afc8d623c6" />




---

## 6. Draw a rectangle.

```python
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)

plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

### Output

<img width="800" height="492" alt="image" src="https://github.com/user-attachments/assets/283ec3df-6d8d-46f3-b8db-2581013d8816" />



---

## 7. Add text to the image.

```python
text_img = cv2.putText(img_rgb, "AJAY S", (10, 40), cv2.FONT_HERSHEY_SIMPLEX, 1.2, (0, 0, 255), 2)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="753" height="453" alt="image" src="https://github.com/user-attachments/assets/17949387-0ef5-4318-8693-f45d34c8dc6e" />


---

## 8. Convert the image to HSV.

```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

### Output

<img width="726" height="527" alt="image" src="https://github.com/user-attachments/assets/a8959fa0-e56a-4c42-a34d-8aad22c86385" />



---

## 9. Convert the image to Grayscale.

```python
gray = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)

plt.imshow(gray, cmap="gray")
plt.axis("off")
plt.show()
```

### Output

<img width="717" height="495" alt="image" src="https://github.com/user-attachments/assets/73aa179a-8be7-486f-9844-05c5a273c6ef" />


---

## 10. Convert the image to YCrCb.

```python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

### Output

<img width="733" height="517" alt="image" src="https://github.com/user-attachments/assets/95268947-b370-42e2-9ef0-341d51d46df7" />




---

## 11. Convert HSV back to RGB.

```python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)

plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

### Output
<img width="672" height="502" alt="image" src="https://github.com/user-attachments/assets/7e78630d-7ca2-47a4-9300-1246b4afac35" />



---

## 12. Access and modify pixel values.

```python
image[50:200, 100:300] = [255, 255, 255]
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("on")
plt.show()
```

### Output

<img width="778" height="531" alt="image" src="https://github.com/user-attachments/assets/5c74ca79-e2db-434f-b521-487a680c1872" />


---

## 13. Resize the image.

```python
resized_image = cv2.resize(image, (768 // 2, 600 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)

plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

### Output

<img width="697" height="525" alt="image" src="https://github.com/user-attachments/assets/90158ace-4e06-4a41-9032-1b4f5722b750" />



---

## 14. Crop the image.

```python
roi = image[50:350, 50:350]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)

plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

### Output


<img width="722" height="480" alt="image" src="https://github.com/user-attachments/assets/04009869-eb00-4c8a-9b4f-a52df0336530" />


---

## 15. Flip the image horizontally.

```python
flipped_horizontally = cv2.flip(image, 1)

flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```

### Output

<img width="758" height="498" alt="image" src="https://github.com/user-attachments/assets/f8a30425-0290-423e-bfda-f8f1fa71e0c5" />



---

## 16. Flip the image vertically.

```python
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

### Output

<img width="671" height="495" alt="image" src="https://github.com/user-attachments/assets/30cf34c2-9d6e-48c9-b860-6d11d94ea4d4" />



---

# Result

Thus, the image was successfully read, displayed, modified using various OpenCV drawing functions, converted into different color spaces, resized, cropped, and flipped successfully using Python and OpenCV.
