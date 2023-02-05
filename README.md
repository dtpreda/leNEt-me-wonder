# Le(Ne)t Me Wonder

This repository contains a short notebook with the code for a MobileNetV2 model trained on the [Wonders of the World Image Dataset](https://www.kaggle.com/datasets/balabaskar/wonders-of-the-world-image-classification) from Kaggle. The goal is to classify each image into one of 12 classes, with some of the old and new wonders of the world among them.

## Usage

The notebook is self-contained and can be run from top to bottom. The only requirement is to have the dataset in the same directory as the notebook, under *`data/Wonders of World`*. The dataset can be downloaded from the link above.

There is also a pre-trained model included, `model.h5`.

## Results

The model is comprised of a MobileNetV2 base with a global average pooling layer, a dropout layer and a dense layer with 12 units and softmax activation. The model was compiled with the Adam optimizer and sparse categorical crossentropy loss.

The model was trained on 10 epochs and using class weights to account for class imbalance. It attained a test accuracy of 93%. 

Only the new layers were trained, the base was frozen. As such, only 15k parameters were trained for this specific task.