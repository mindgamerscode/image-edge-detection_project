# Edge Detection from Image(about project)

=> (Image Edge Detection Techniques using OpenCV)


Code Implementation:
* Importing necessary libraries: OpenCV and Matplotlib.
    -> OpenCV (Open Source Computer Vision Library) is a popular open-source computer vision and machine learning software library. It provides various functions for image processing, including reading and 
       manipulating images, performing transformations, and implementing various algorithms for object detection, recognition, and more.
    -> Matplotlib is a widely-used plotting library in Python that provides a MATLAB-like interface for creating 2D plots and visualizations. It's commonly used to display images, plot graphs, histograms, and 
       more.

* Loading the image using OpenCV:
    -> The cv2.imread() function from the OpenCV library is used to read an image file from the disk.
    -> The image is loaded as a NumPy array, which represents the image as a grid of pixel values.
    -> The image file path ("img.png" in this case) is provided as an argument to the imread() function.


Image Processing Steps:
* Step 1: Horizontal Sobel: Detecting edges using horizontal Sobel filter.
    -> The horizontal Sobel filter is a convolution kernel used for edge detection in images.
    -> It calculates the gradient of the image intensity in the horizontal direction, emphasizing vertical edges.
    -> In the code, cv2.Sobel() function is applied with parameters specifying the input image (img), data type (cv2.CV_64F for 64-bit floating-point), horizontal direction (1), vertical direction (0), and kernel 
       size (5x5 in this case).

* Step 2:  Vertical Sobel: Detecting edges using vertical Sobel filter.
    -> Similar to the horizontal Sobel filter, the vertical Sobel filter calculates the gradient of the image intensity but in the vertical direction, highlighting horizontal edges.
    -> This filter is applied using the same cv2.Sobel() function, with parameters adjusted to detect vertical edges.

* Step 3:   Laplacian: Applying Laplacian filter for edge detection.
    -> It calculates the rate of change of intensity in the image, which helps identify regions of rapid intensity change, indicating the presence of edges.
    -> The Laplacian filter is applied using the cv2.Laplacian() function, which takes the input image (img) and the data type (cv2.CV_64F).

* Step 4: Canny Edge Detection: Implementing Canny edge detection algorithm.
    -> It involves smoothing the image with a Gaussian filter, finding the intensity gradients, applying non-maximum suppression to thin the edges, and finally applying hysteresis to detect strong and weak edges.
    -> In the code, cv2.Canny() function is used with parameters specifying the input image (img), thresholds for gradient magnitude (50 and 150), which determine the minimum and maximum intensity gradients 
       considered as edges.
