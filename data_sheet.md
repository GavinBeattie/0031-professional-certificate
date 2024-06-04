# Datasheet for [simpsons-mnist](https://github.com/alvarobartt/simpsons-mnist)
The following datasheet accompanies the model card. It contains a summary of the origins of the dataset and how it has been used to support my portfolio project submission (this project).

[Readme](README.md) | [Jupyter Notebook](portfolio-project-submission.ipynb) | [Datasheet](data_sheet.md) | [Model Card](model_card.md)

## Motivation
- The dataset was created to train neural networks for educational purposes.
- The dataset was created by [Alexandre Attia](https://github.com/alexattia), who created the dataset to be more engaging than the traditional MNIST datasets. It is assumed to be self-funded, and in his own words, it is deliberately "small and dirty" compared to other MNIST datasets.

## Composition
- The instances within the dataset are images of Simpsons characters comprising a training set of 8,000 examples and a testing set of 2,000 examples.
- Because it is a relatively small dataset, instances are provided in both greyscale and RGB colour. As a demo set, this was one of the attractions.
- It is suitable for training Convolutional Neural Networks (CNNs), and there is some demo code to use the dataset with TensorFlow and PyTorch packages.

## Collection process
- The data was gathered and uploaded approximately three years ago.

## Preprocessing/cleaning/labelling
- There is no direct information available about steps taken regarding preprocessing/cleaning/labelling of the data. However, because the images are reasonably well-centred on the characters, an element of processing is assumed to have been done.
- There is no additional "raw" data provided.

## Uses
- Educational purposes for training neural networks on almost any computer.
- The dataset deliberately contains 10 classes, making it suitable for the task at hand.
- Because it contains only cartoon characters, there is little to no risk to persons from using it.

## Distribution
- The dataset has been publicly available for three years.
- The dataset is provided largely "as is" under an Attribution-NonCommercial-ShareAlike 4.0 International license.

## Maintenance
- [Alexandre Attia](https://github.com/alexattia) initially created and hosts the dataset. It is not expected to be maintained or updated in the future.
