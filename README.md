# Facial Keypoints Detection
Facial Keypoints Detection


This repository contains the Facial Keypoint Detection project, which is the first project in the Computer Vision Nanodegree from Udacity.

The Facial Keypoint Detection project uses 6 layer LeNet style convolutional neural network (CNN) to find 68 facial keypoints on a face. Facial Keypoints are also called Facial Landmarks which generally specify the areas of the nose, eyes, mouth, etc on the face, classified by 68 key points, with coordinates (x, y), for that face. The keypoints are positioned on the features of a face, such as the eyebrow, nose, and mouth. The points could therefore be used in a number of applications including emotion detection and facial feature classification.

# Dataset:
Udacity provided YouTube Faces Dataset. It contains 3,425 face videos designed for studying the problem of unconstrained face recognition in videos. These videos have been fed through processing steps and turned into sets of image frames containing one face and the associated keypoints.

# Training and Test Data:
Udacity: "This facial keypoints dataset consists of 5770 color images. All of these images are separated into either a training or a test set of data. 3462 of these images are training images, for you to use as you create a model to predict keypoints.
2308 are test images, which will be used to test the accuracy of your model."


# Pre-Processing the Data:
In order to feed the data(images) into the neural network, we have to transform the images into a fixed dimensional size and a standard color range by converting the numpy arrays to Pytorch Tensors(for faster computation).

# Transforms:
Normalize: to convert a color image to grayscale values with a range of [0,1] and normalize the keypoints to be in a range of about [-1, 1]
Rescale: to rescale an image to a desired size.
RandomCrop: to crop an image randomly.
ToTensor: to convert numpy images to torch images.


# Second jupyter notebook 
# 2. Define the Network Architecture.ipynb

Define the CNN Architecture: See models.py


