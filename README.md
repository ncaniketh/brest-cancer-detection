# Breast-cancer-classification

Breast Cancer Classification using CNN and transfer learning

## INTRODUCTION

If you find this code useful in your research, please consider citing the blog:

## STEPS


      Problem Statement
Breast cancer is the second most frequent cancer in women and men globally. In 2012, it factored about 12 percent of all latest cancer cases and 25 percent of women’s total cancers.

Breast cancer arises when cells in the breast start to develop out of control. These cells usually grow a tumor that can frequently be seen on an x-ray or considered a lump. The tumor is malignant (cancer) if the cells can expand into (invade) encompassing tissues or increase (metastasize) to different sections of the body.

     The Hurdle
Construct an algorithm to automatically classify whether a victim is experiencing breast cancer or not by studying biopsy photographs.

     Downloading DataSet
The data for the plan can be obtained here. It is a binary classification problem.

We have 277,524 samples with dimensions 50 x 50 (198,738 IDC negative and 78,786 IDC positive)

Loading Image
Become a Full-Stack Data Scientist
Get Flat INR 8500 ($112) OFF + 4- Data Engineering Courses Absolutely FREE
breast cancer classification dataset
Source: https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/
Where (a & b) belongs to Benign Samples and (c & d) belongs to Malignant Samples.

     Deep Learning To Rescue
 1.Input
Input is a matrix of pixel values in the configuration of [WIDTH, HEIGHT, CHANNELS].

     2.Convolution Layer
The objective of this layer is to sustain a feature map. Typically, we commence with a base estimate of filters for low-level feature detection. The more distant we go within CNN, the added filters we use to identify high-level features. Feature detection is based on ‘examining’ the input with a presented dimension filter and implementing matrix computations to infer a feature map.

     3.Pooling Layer
This layer aims to implement spatial variance, which means that the system will be proficient in identifying an object even when its appearance differs somehow. The pooling layer will do a downsampling procedure accompanying the spatial dimensions (width, height), resulting in the product such as [16x16x12] for pooling_size=(2, 2).

    4.Fully Connected Layer
In a fully connected layer, we flatten the product of the end convolution layer and combine every node of the prevailing layer with the separate nodes of the subsequent layer.

## Data

The dataset can be downloaded from [here](https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/). This is a binary classification problem. I split the data as shown-

```
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
```    

## Environment and tools

1. Jupyter Notebook
2. Numpy
3. Pandas
4. Scikit-image
5. Matplotlib
6. Scikit-learn
7. Keras

## Installation

`pip install numpy pandas scikit-image matplotlib scikit-learn keras`

`jupyter notebook`

## Model

![model](images/image6.png)

## Results

### Loss/Accuracy vs Epoch

![loss/accuracy](images/image1.png)

![loss/accuracy](images/image2.png)

### Confusion Matrix

![roc-auc](images/image3.png)

### ROC-AUC curve

![roc-auc](images/image4.png)

### Correct/Incorrect classification samples

![results](images/image5.png)


![results](images/image7.png)

The model is able to reach a validation accuracy of 98.3%, precision 0.65, recall 0.95, f1 score of 0.77 and ROC-AUC as 0.692.
