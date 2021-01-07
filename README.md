# Overview

This repo that contains projects I either did alone or contributed heavily. Each project is within it's respective folder. For specific project code email morgan.nanez@gmail.com.

## Classes in this repo
DS100: Principles and Techniques of Data Science <br>
CS194: Computer Vision <br>
CS161: Cyber Security <br>

## Influential Factors on Women’s Education in Indonesia [ds100_final]
Myself and two others explore the factors that best determine what educational level a woman has achieved based on the 1987 National Indonesia Contraceptive Prevalence Survey. We used data science techniques to compare and contrast the prediction success or failure for 3 common prediction models:  Multi-Class Logistic Regression, Decision Tree, and Random Forest modeling.

## Colorizing the Prokudin-Gorskii photo collection [cs194_proj1]

The goal of the project is to take the digitized Prokudin-Gorskii glass plate images and apply image processing techniques to automatically produce a color image. The basic method is to extract the three color channel images, place them on top of each other, and align them so that they form a single RGB color image.

## Fun with Filters and Frequencies [cs194_proj2]

In this project, I convolve a gaussian filter with an image's Dx and Dy, creating a Derivative of a gaussian filter (DoG). I use the DoG to automatically straighten an image. I then use the unsharp masking technique to "sharpen" images. I do this by subtracting the blurred version from the original image to get the high frequencies of the image and add these frequencies back onto the original image. I then create hybrid images by blending the high frequency portion of one image with the low-frequency portion of another. I show this further by using Gaussian and Laplacian Stacks. Finally, I blend two images seamlessly using a multi resolution blending.  

## Face Morphing and Modeling a Photo Collection [cs194_proj3]

The goal of the project is to produce a "morph" animation of my face into someone else's face, compute the mean of a population of faces and extrapolate from a population mean to create a caricature of yourself.

## Face Key-point Detection with Neural Networks [cs194_proj4]

Here, I use convolutional neural networks to automatically detect facial keypoints. I begin by just detecting a person's nose tip, then eventually to detect 56 facial key points. I used PyTorch to create a custom DataLoader and preformed pre-processing data augmentation to prevent the model from overfitting. I then created a convolutional neural network and trained it on the IMM Face Database

## Autostitiching Photo Mosaics [cs194_proj5]

This project is all about stitching together many photographs to create larger composite images. I begin by perfecting my blending and warping algorithem on self selected correspondence points. For each image, I recover  the homographies, warp the image based on the recovered transformation, then blend the images into a mosaic. To automate this process of selecting corresspondencepoints, I first detect corner features of an image and extract a Feature Descriptor for each image. I match the feature descriptors between two images then use 4-point RANSAC to compute a robust homography estimate. I follow the same steps for warping and blending, using the proper homogrpaghy estimate, to create a beauitufl mosaic.

## Reimplement: A Neural Algoritm of Artistic Style [cs194_proj6]
In this project, I reimplement Gatys et al's 2015 paper. The goal is to extract the style of one image and apply it to the content of another image. I do this by using the feature space provided by PyTorch's pretrained VGG19 model. For content activation, I used the second convolutional layer in the 4th block. For style activations,I used the first convolutional layer in each of the 5 blocks, as described in the paper. For faster results, I  utilized the GPU on Google Colab.


## An End-to-End Encrypted File Sharing System [cs161_proj2]

In a team of three, we designed and implement a secure file sharing system in Go. Users of our application will launch our client and provide their username and password. Once authenticated, they will use our client to upload and download files to/from the server. Our client will be the interface through which users can interact with the files stored on the server, such as sharing a file. Our design ensures confidentiality and integrity of files in addition to the basic file-sharing functionality.
