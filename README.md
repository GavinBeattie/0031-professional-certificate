# 0031-professional-certificate
Portfolio Project for Professional Certificate in Machine Learning and Artificial Intelligence

## Executive Summary (100-word description)
The included notebook trains a LeNet-5 model using PyTorch. Hyperparameters such as learning rate, epochs, and momentum are optimised with Hyperopt.

This code runs on Apple MacBook Pro and Nvidia Jetson Nano hardware – it probably works on other systems too! The dataset consists of 10,000 images featuring characters from The Simpsons.

In the final code block, the built-in camera of the MacBook Pro and an external webcam with the Jetson Nano are used to capture a series of image snapshots and predict the character from the images.

End-to-end, it functions as a comprehensive solution, a hopefully a bit of fun!

## Structuring your GitHub repository
I used Visual Studio Code for editing and source control. This repository is initially public. The README started as an accompanying log and was tidied up into documentation at the end.

A single Jupyter notebook is included with some initial sketches. This has been entered into source control, which was quite painless. The .gitignore file is configured to exclude raw image folders from being uploaded. Instead, links to their source locations and providers are included.

For the structure, I am adhering to the headings outlined in the project brief/description.
After uploading my Jupyter notebook, GitHub detected the language used, which is nice. The repository is marked public and includes an MIT license. The model is the original LeNet-5, as covered in the course, adapted to work with Hyperopt for automated hyperparameter tuning. Additionally, the model has been deployed on both an Apple MacBook Pro and Nvidia Jetson Nano hardware. There is also a final evaluation using a camera snapshot to test the model.

## Finding a dataset
I originally wanted to create my own dataset from images suited to an industry classification task. If I have time, I will revisit this activity at the end or after the course concludes. My focus is on getting a working Convolutional Neural Network (CNN) using automated hyperparameter tuning (AutoML). To this end, I have been studying the Hyperopt documentation and tutorials. I chose Hyperopt because it was the first package listed in the selected article I reviewed [1]. I hope to explore the other two packages (pySOT and TurBO) later.

Throughout the course, we have been introduced to various datasets from the machine learning domain. For reasons of speed and expediency, I am staying within familiar territory and using the Mitchell faces and Fashion-MNIST datasets, along with a third new dataset. The new dataset was chosen for two reasons: firstly, I wanted something fun, and secondly, I needed a dataset smaller than Fashion-MNIST but larger than the Mitchell faces dataset. This was important because I expected to automatically tune hyperparameters and needed enough data to achieve good accuracy, but not so much data that time and resources would be overwhelmed – a trade-off!

Initially, I planned to load the dataset in greyscale to match the previous exercises and begin tuning. However, I decided to use colour images (and update the model accordingly). Practically, the images are all 28x28, which requires fewer changes for experimenting with automated hyperparameter tuning. My goal is to include extensions to Hyperopt and GPU hardware and submit a fun portfolio project that is extensible to other image applications.

The dataset I chose is called Simpsons-MNIST. It is provided in both colour and greyscale, has 10 classes, and an 80:20 train:test split. The total number of images is 10,000, a reduction from the 60,000 images in the Fashion-MNIST dataset, to reduce training time. The data was randomised on load using data loader functions.

### Experiments
I decided to follow the structure of the selected article to make this more like an experiment, demonstrating the benefits of the Hyperopt package. I discussed this in my critique of the selected article, and it feels worthwhile and appropriate to try it out.

I have moved away from my original rail industry-inspired idea. Although it would have been a good exploration of Bayesian optimisation, there were too many unknowns to start with certainty for this exercise. It also lacked the ties to CNNs and hardware that I find exciting. I have defined learning rate, epochs, and momentum as the three hyperparameters to tune using Hyperopt.

## Choosing a model
Selecting a model was relatively straightforward. I already had the submission file for LeNet-5, which I had used previously for Mitchell faces. However, I found its optimisation and results somewhat lacking.

Having undergone a crash course in Hyperopt, I've decided to take the base LeNet-5 model developed during the course and enhance it with Hyperopt Bayesian optimisation.

## Hyperparameter optimisation
As mentioned in the previous section, my experience with automated hyperparameter tuning is limited, having only completed the first two tutorials after being introduced to it in the selected article. With no preconceived notions about the performance results, I embarked on this journey. My initial impressions of the package are positive; it seems relatively easy to understand. However, I've noticed that the documentation appears to be evolving alongside the package itself.

I recently acquired an Nvidia Jetson Nano 4GB, and I've managed to set up the prerequisite libraries to create an environment. Although it's still early days, I've made enough progress to run PyTorch on the GPU, providing a valuable benchmark comparison against the CPU of my MacBook Pro.

While working through the course notebooks, I discovered the option to transition to a GPU device, prompting me to explore this aspect further. Setting up a working environment for Jupyter notebooks on the Jetson Nano required some effort, which I plan to revisit and document thoroughly.

## Performance metrics and results
Within the notebook, I've included some indicative metrics to demonstrate the impact of Hyperopt tuning. The primary performance measure is accuracy, which I've then extended to a real-world application based on camera input.

The results obtained from applying the Hyperopt package are remarkable. Starting from an initial accuracy of 20%, the tuning process increased it to just over 70%, a satisfactory outcome.

I've tried to heavily comment the code within the notebook. The model itself can be easily extracted, along with the Hyperopt hyperparameters, which could prove more useful for future experimentation.

## References:
1. [Selected Article](https://valohaichirpprod.blob.core.windows.net/papers/duxiaoman.pdf)
1. [MNIST-like Simpsons dataset](https://github.com/alvarobartt/simpsons-mnist)
