# Edge Detection from Image

import cv2
import matplotlib.pyplot as plt

img = cv2.imread("img.png")
#img = cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
#plt.imshow(img)

img1 = cv2.Sobel(img,cv2.CV_64F,1,0,5) #Horizontal Sobel 
img2 = cv2.Sobel(img,cv2.CV_64F,0,1,5) #Vertical Sobel
img3 = cv2.Laplacian(img,cv2.CV_64F)
img4 = cv2.Canny(img,50,150)



plt.subplot(2,3,1),plt.imshow(img,cmap="gray"),plt.title("original image")
plt.subplot(2,3,2),plt.imshow(img1,cmap="gray"),plt.title("Horizontal Sobel")
plt.subplot(2,3,3),plt.imshow(img2,cmap="gray"),plt.title("Vertical Sobel")
plt.subplot(2,3,4),plt.imshow(img3,cmap="gray"),plt.title("Laplacian")
plt.subplot(2,3,5),plt.imshow(img4,cmap="gray"),plt.title("Canny")
