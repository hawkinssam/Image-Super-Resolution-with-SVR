# Image-Super-Resolution-with-SVR

This project looks at image super-resolution using Support Vector Regression (SVR). Super Resolution is the concept of attempting to increase the resolution of an image, while losing as little detail as possible in the process. Traditionally, interpolation is used to increase resolution of an image, and is usually considered "good enough" for the intended purposes of increasing resolution. Machine learning techniques have been used to try and improve on the performance of interpolation, and SVR is one method that has shown success. 

Support vector regression is a method that attempts to create support vectors that best separate data of different pixel intensities. In most cases with images, a linear SVR model will not be adequate, as the patterns of pixel values are certainly not linear. Thus, a kernel function needs to be used to map the data into a higher dimension, where linear regression can then be completed. 

To create training data, we start with a high resolution (HR) image. This image is first downsampled using bicubic interpolation, then upsampled back to the original size, also using bicubic interpolation. In downsampling and upsampling, some fine details from the original HR image are lost, making the new image of the correct size, but blurry. To create training feature vectors for SVR, an m x m "patch" is slid over every pixel in the blurry image. The patches are vectorized, either row by row, or column by column. Each vectorized patch centered at the input image index (i,j) is the feature vector that corresponds to the single pixel value at index (i,j) in the original high resolution image. Thus, each output pixel value in the HR image corresponds to an m^2 size feature vector in the interpolated image. An SVR model is trained to predict a single pixel value for each patch given a collection of patches from an interpolated image. 

The USC-SIPI Image Database [^1] was used to test the trained SVR model on varying images. 

The project was completed using Google Colab, so it may be easiest to have the AT&T faces dataset in your Google Drive, and have your Drive mounted.




[^1]: [online] at https://sipi.usc.edu/database/
