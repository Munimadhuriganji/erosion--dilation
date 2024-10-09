## Implementation-of-Erosion-and-Dilation
# Aim
To implement Erosion and Dilation using Python and OpenCV.

# Software Required
Anaconda - Python 3.7
OpenCV
# Algorithm:
# Step1:
Import the necessary pacakages

# Step2:
Create the text using cv2.putText

# Step3:
Create the structuring element

# Step4:
Erode the image

# Step5:
Dilate the Image

# Program:
```
Developed By:Ganji Muni Madhuri
Ref No:212223230060
```
```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Create a blank image
image = np.zeros((300, 600, 3), dtype="uint8")


# Step 2: Create the text using cv2.putText
text = "OpenCV Demo"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)

# Step 3: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Step 4: Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)

# Step 5: Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)

# Plot the original, eroded, and dilated images using Matplotlib
plt.figure(figsize=(10, 5))

#Original Image:
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

#Eroded Image:
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

#Dilated Image:
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

plt.tight_layout()
plt.show()
```

## Output:
# Display the input Image

![image](https://github.com/user-attachments/assets/9e44b105-225b-4564-b857-b9ae019d2e88)

# Display the Eroded Image
![image](https://github.com/user-attachments/assets/13351b4a-aeb0-4da0-a50b-1f26e43a89ea)



# Display the Dilated Image
![image](https://github.com/user-attachments/assets/f7287c9b-39c9-444b-91e7-1e088d549ba9)




# Result
Thus the generated text image is eroded and dilated using python and OpenCV.
