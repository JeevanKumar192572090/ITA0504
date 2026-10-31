import cv2
import matplotlib.pyplot as plt

# Read the original image (or use your uploaded one)
img_bgr = cv2.imread(image_path)
img_rgb = cv2.cvtColor(img_bgr, cv2.COLOR_BGR2RGB)

# Apply Gaussian Blur
# ksize (width, height) must be positive and odd. sigmaX is the standard deviation.
ksize = (15, 15) 
img_blur_cv = cv2.GaussianBlur(img_rgb, ksize, sigmaX=0)

# Display the original and blurred images side by side
fig, axes = plt.subplots(1, 2, figsize=(10, 5))
axes[0].imshow(img_rgb)
axes[0].set_title('Original Image')
axes[0].axis('off')

axes[1].imshow(img_blur_cv)
axes[1].set_title('Blurred Image (OpenCV)')
axes[1].axis('off')

plt.tight_layout()
plt.show()
