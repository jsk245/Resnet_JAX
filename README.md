## Info
This is a recreation of the ResNet paper that can be viewed here: https://arxiv.org/abs/1512.03385. The ResNet-50 model was originally used to perform image classification, and it is a common model to copy weights from to use in other projects. The deepmind JAX-based haiku python library was used for recreation, and the model was trained using Google Colab. I trained the model for about 10 minutes on the cifar-100 dataset and managed to achieve 33% accuracy on the test set and 97% accuracy on the training set.

## ToDo
- train model overnight to see how high the accuracy is afterwards
- take this model and train on ImageNet for comparison with the original paper
- fix excess RAM usage during training
