# brest-cancer-detection
     importing packages


import json
import math
import os
import cv2
from PIL import Image

     READING DATA 

#Transfer 'jpg' images to an array IMG
def Dataset_loader(DIR, RESIZE, sigmaX=10):
    IMG = []
    read = lambda imname: np.asarray(Image.open(imname).convert("RGB"))
    for IMAGE_NAME in tqdm(os.listdir(DIR)):
  The dataset can be downloaded from here. This is a binary classification problem. I split the data as shown-
  dataset train
  benign
   b1.jpg
   b2.jpg
   //
  malignant
   m1.jpg
   m2.jpg
   //  validation
   benign
    b1.jpg
    b2.jpg
    //
   malignant
    m1.jpg
    m2.jpg
    //...
    
    Environment and tools
Jupyter Notebook
Numpy
Pandas
Scikit-image
Matplotlib
Scikit-learn
Keras

     #1.Input
Input is a matrix of pixel values in the configuration of [WIDTH, HEIGHT, CHANNELS].

#2.Convolution Layer
The objective of this layer is to sustain a feature map. Typically, we commence with a base estimate of filters for low-level feature detection. The more distant we go within CNN, the added filters we use to identify high-level features. Feature detection is based on ‘examining’ the input with a presented dimension filter and implementing matrix computations to infer a feature map.

     #3.Pooling Layer
This layer aims to implement spatial variance, which means that the system will be proficient in identifying an object even when its appearance differs somehow. The pooling layer will do a downsampling procedure accompanying the spatial dimensions (width, height), resulting in the product such as [16x16x12] for pooling_size=(2, 2).

     #4.Fully Connected Layer
In a fully connected layer, we flatten the product of the end convolution layer and combine every node of the prevailing layer with the separate nodes of the subsequent layer.

     Implementation
First, we load all the libraries and packages.

