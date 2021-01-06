# Smoothed Sobel gradient and Laplacian for Greater Sharpening

## The narrow dynamic range of the intensity levels and high noise content make this image difficult to enhance. The strategy we will follow is to utilize,

### 1. The Laplacian to highlight fine detail(Second Derivative for Image Sharpening)

Resultant image is sharpened but still noisy. To reduce the noise a median filter can be used. However, median filtering is a nonlinear process capable of removing image features. This is unacceptable in medical image processing.

### 2. A smoothed version of the gradient image to mask the Laplacian image(Original + Laplacian).

The response of the gradient to noise and fine details is lower than the Laplacian’s and can be lowered further by smoothing the gradient with an averaging filter.

### 3. Increase the dynamic range of the intensity levels by using an intensity transformation.

Histogram equalization is not likely to work well on images that have dark intensity distributions like our images have here. Histogram specification could be a solution, but the dark characteristics of the images with which we are dealing lend themselves much better to a power-law transformation i.e. Gamma Correction
