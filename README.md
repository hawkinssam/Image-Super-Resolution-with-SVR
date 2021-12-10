# Image-Super-Resolution-with-SVR

This project looks at image super-resolution using support vector regression. Super Resolution is the concept of attempting to increase the resolution of an image, while losing as little detail as possible in the process. Traditionally, interpolation is used to increase resolution of an image, and is usually considered "good enough" for the intended purposes of increasing resolution. Machine learning techniques have been used to try and improve on the performance of interpolation, and Support Vector Regression (SVR) is one method that has shown success. 

Support vector regression is a method that attempts to create support vectors that best separate data of different pixel intensities. In most cases with images, a linear SVR model will not be adequate, as the patterns of pixel values are certainly not linear. Thus, a kernel function needs to be used to map the data into a higher dimension, where linear regression can then be completed. 

To create training data, 

The project was completed using Google Colab, so it may be easiest to have the AT&T faces dataset in your Google Drive, and have your Drive mounted.

If implementing this method in the .py file format, it may be best to either download the data to your desktop or use Kaggle to load in the dataset. 


