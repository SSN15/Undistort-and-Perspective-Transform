![original](https://github.com/SSN15/Undistort-and-Perspective-Transform/blob/master/original.png)
The goal is to generate output like the image shown above. To do that, we need to write a function that takes your distorted image as input and completes the following steps:

1. Undistort the image using cv2.undistort() with mtx and dist
2. Convert to grayscale
3. Find the chessboard corners
4. Draw corners
5. Define 4 source points (the outer 4 corners detected in the chessboard pattern)
6. Define 4 destination points (must be listed in the same order as src points!)
7. Use cv2.getPerspectiveTransform() to get M, the transform matrix
8. use cv2.warpPerspective() to apply M and warp your image to a top-down view
