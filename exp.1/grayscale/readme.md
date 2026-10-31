import cv2
import matplotlib.pyplot as plt

try:
    # Read the uploaded image using OpenCV
    img_bgr = cv2.imread(image_path)

 
except NameError:
    print("Please run the upload cell above first to upload your image.")
except Exception as e:
    print(f"An error occurred: {e}")
