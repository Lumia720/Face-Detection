# Facial Keypoints Detection
Facial Keypoints Detection


This repository contains the Facial Keypoint Detection project, which is the first project in the Computer Vision Nanodegree from Udacity.

The Facial Keypoint Detection project uses 6 layer LeNet style convolutional neural network (CNN) to find 68 facial keypoints on a face. Facial Keypoints are also called Facial Landmarks which generally specify the areas of the nose, eyes, mouth, etc on the face, classified by 68 key points, with coordinates (x, y), for that face. The keypoints are positioned on the features of a face, such as the eyebrow, nose, and mouth. The points could therefore be used in a number of applications including emotion detection and facial feature classification.



![](https://github.com/Lumia720/Facial-Keypoints-Detection/blob/master/images/obama_michelle.png)

Topic: supervised deep neural network


# First Jupyter notebook 1. Load and Visualize Data.ipynb

Steps:
1) Dataset:
Udacity provided YouTube Faces Dataset. It contains 3,425 face videos designed for studying the problem of unconstrained face recognition in videos. These videos have been fed through processing steps and turned into sets of image frames containing one face and the associated keypoints.

2) Training and Test Data:
Udacity: "This facial keypoints dataset consists of 5770 color images. All of these images are separated into either a training or a test set of data. 3462 of these images are training images, for you to use as you create a model to predict keypoints.
2308 are test images, which will be used to test the accuracy of your model."


3) Pre-Processing the Data:
In order to feed the data(images) into the neural network, we have to transform the images into a fixed dimensional size and a standard color range by converting the numpy arrays to Pytorch Tensors(for faster computation).

4) Transforms:
Normalize: to convert a color image to grayscale values with a range of [0,1] and normalize the keypoints to be in a range of about [-1, 1]
Rescale: to rescale an image to a desired size 250X250.
RandomCrop: to crop an image randomly 224X224.
ToTensor: to convert numpy images to torch images.

5) Create the Transformed Dataset


# Second Jupyter notebook // 2. Define the Network Architecture.ipynb

Steps:

1) Define the CNN Architecture: See models.py

2) Create the transformed Facial Keypoints Dataset with Transforms as previously

3) Define Batch size and load data

4) Train the CNN Model and Track the loss

5) Save the model into Saved_models (too large size to pist here)


# Third Jupyter notebook // 3. Facial Keypoint Detection, Complete Pipeline.ipynb

Steps
1) Detect faces in any image using Haar Cascade Detector in the project

2) Transform each detected face into an input Tensor: for each detected face:
Convert the face from RGB to grayscale, Normalize the grayscale image so that its color range falls in [0,1] instead of [0,255], Rescale the detected face to be the expected square size for your CNN (224x224, suggested), Reshape the numpy image into a torch image

3) Detect and display the predicted keypoints



