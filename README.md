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

Installation
pip install numpy pandas scikit-image matplotlib scikit-learn keras

jupyter notebook

Model
model

Results
Loss/Accuracy vs Epoch
loss/accuracy

loss/accuracy

Confusion Matrix
roc-auc

ROC-AUC curve
roc-auc

Correct/Incorrect classification samples
results

results
