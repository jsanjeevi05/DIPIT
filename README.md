```
import cv2

image = cv2.imread('Apollo.jpeg', cv2.IMREAD_GRAYSCALE)

height, width = image.shape
print("Width:", width)
print("Height:", height)

plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off')
plt.show()

cv2.imwrite('Apollo-11-launch.png', image)
import cv2

image_color = cv2.imread('NZ.jpeg', cv2.IMREAD_COLOR)

print("Color Image Shape:", image_color.shape)

image_gray = cv2.cvtColor(image_color, cv2.COLOR_BGR2GRAY)

print("Grayscale Image Shape:", image_gray.shape)

plt.figure(figsize=[10, 10])
plt.imshow(image_gray, cmap='gray')
plt.axis('off')
plt.show()
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('NZ Boat.jpeg', cv2.IMREAD_COLOR)

cropped_img = img[3:500, 3:500]  

resized_img = cv2.resize(cropped_img, None, fx=2, fy=2, interpolation=cv2.INTER_LINEAR)

flipped_img = cv2.flip(resized_img, 1)

plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1]) 
plt.axis('on')
plt.show()
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('Apollo.jpeg')

text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_PLAIN
font_scale = 3
font_color = (255, 255, 255) 
font_thickness = 2

(text_width, text_height), _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_width)   
text_y = image.shape[0] - 50 

cv2.putText(image, text, (text_x, text_y), font_face, font_scale, font_color, font_thickness)


rect_color = (255,0,255)  
top_left = (100,180) 
bottom_right = (image.shape[1] - 100, image.shape[0] - 200) 

cv2.rectangle(image, top_left, bottom_right, rect_color, 3)

plt.figure(figsize=[10, 10])
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('NZ.jpeg', cv2.IMREAD_COLOR)

print(image.shape)

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

print(gray_image.shape)

plt.figure(figsize=(10, 8))
plt.imshow(gray_image, cmap='gray')
plt.axis('on')
plt.show()
```

##Output:

![image](https://github.com/user-attachments/assets/82b669f4-d4bd-4e21-bbaa-64c70c6d084e)
![image](https://github.com/user-attachments/assets/5600fd96-4e91-4189-b2db-01c6b9a70412)
![image](https://github.com/user-attachments/assets/4e47435a-88c4-4c3f-a9e9-4c4ee716698c)
![image](https://github.com/user-attachments/assets/37a44e79-0fc1-4c5c-83bf-f5ca6588a01c)
![image](https://github.com/user-attachments/assets/0235fb2a-2993-4602-a4a5-6e1cb0929827)





