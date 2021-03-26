# Recyclenet
>Trash classification AI.

This repo is a collection of notebooks that I've created for the purposes of trash classification.

Some notebooks use the [6-catagory trashnet-resized dataset](https://github.com/garythung/trashnet) while others use the 
the [12-catagory garbage-classification dataset](https://www.kaggle.com/mostafaabla/garbage-classification).
These notebooks heavily draw upon code examples provided by [Tensorflow](https://www.tensorflow.org/tutorials)

## Notebooks

All of the notebooks are designed to run in Google Colab.

A major concern of using it is that it imposes ram limits. In order to avoid these, a small batch and image size is used and the dataset is sometimes not cached or optimised like
what you would typically see.

Every effort has been made to stay just under these limits while having a speedy model.

A summary of the notebooks is provided below:

|Notebook|Dataset|Peak Accuracy|Image size|Batch size|Details
---|---|---|---|---|---
|main.ipynb|12 catagory|79.31%|100x100|10|Decrease the training rate once it gets to around 75% or so accuracy (possibly due to overfitting). This uses the standard convolutional network approch, with data augmentation and dropout.
|main2.ipynb|6 catagory|90.30%|224x224|32|Same as above (but does not use a convolutional layer). Uses transfer learning with MobileNetV2 for higher accuracy. [Model weights](https://github.com/TinyTinfoil/recyclenet/blob/main/model%20(2).h5) are provided.

