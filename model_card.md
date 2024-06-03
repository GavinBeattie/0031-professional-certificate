# Model Card

A lightweight model to predict chracters from The Simpsons captured by a camera on a MacBook Pro or Jetson Nano.

Not real-time, yet. But relatively easilly adapted.

## Model Description

**Input:** Describe the inputs of your model 
28x28 RGB pixel values.

**Output:** Describe the output(s) of your model
10-class character prediction.

**Model Architecture:** Describe the model architecture you’ve used
LeNet-5 implemented with PyTorch. Convolutional Neural Network.

## Performance

The performance was optimised with the Hyperopt package. The trial results are included with optimal values for learning rate, momentum and epochs.

## Limitations

The model is only expecting characters from The Simpsons. It has not been tested with rotated images.

## Trade-offs

The performance is reasonable ~70% accuracy. However, it would be worth checking the results returned to see how close the next classes were to the max value (the identified class). Performance for 100 trials was undertaken in a reasonable time. Further experimentation with tuning is now easily doable.
