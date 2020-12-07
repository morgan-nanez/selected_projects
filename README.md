# Overview

This repo that contains projects I either did alone from scratch or contributed heavily. Each project is within it's respective folder.

## Influential Factors on Women’s Education in Indonesia [ds100_final]
Myself and two others explore the factors that best determine what educational level a woman has achieved based on the 1987 National Indonesia Contraceptive Prevalence Survey. We used data science techniques to compare and contrast the prediction success or failure for 3 common prediction models:  Multi-Class Logistic Regression, Decision Tree, and Random Forest modeling.

## Colorizing the Prokudin-Gorskii photo collection [cs194_proj1]

The goal of the project is to take the digitized Prokudin-Gorskii glass plate images and apply image processing techniques to automatically produce a color image. The basic method is to extract the three color channel images, place them on top of each other, and align them so that they form a single RGB color image.

## Fun with Filters and Frequencies [cs194_proj2]

In this project, I convolve a gaussian filter with an image's Dx and Dy, creating a Derivative of a gaussian filter (DoG). I use the DoG to automatically straighten an image. I then use the unsharp masking technique to "sharpen" images. I do this by subtracting the blurred version from the original image to get the high frequencies of the image and add these frequencies back onto the original image. I then create hybrid images by blending the high frequency portion of one image with the low-frequency portion of another. I show this further by using Gaussian and Laplacian Stacks. Finally, I blend two images seamlessly using a multi resolution blending.  

## Face Morphing and Modeling a Photo Collection [cs194_proj3]

The goal of the project is to produce a "morph" animation of my face into someone else's face, compute the mean of a population of faces and extrapolate from a population mean to create a caricature of yourself.

## Face Key-point Detection with Neural Networks [cs194_proj4]

Here, I use neural networks to automatically detect facial keypoints. I begin by just detecting a person's nose tip, then eventually to detect 56 facial key points. I used PyTorch to create a custom DataLoader and preformed pre-processing data augmentation to prevent the model from overfitting. I then created a convolutional neural network and trained it on the IMM Face Database

## Autostitiching Photo Mosaics [cs194_proj5]

This project is all about stitching together many photographs to create larger composite images. I begin my perfect my blending and warping algorithem on self selected correspondence points. For each image, I recover  the homographies, warp the image based on the recovered transformation, then blend the images into a mosaic. To automate this process of selecting corresspondencepoints, I first detect corner features of an image and extract a Feature Descriptor for each image. I match the feature descriptors between two images then use 4-point RANSAC to compute a robust homography estimate. I follow the same steps for warping and blending, using the proper homogrpaghy estimate, to create a beauitufl mosaic.
