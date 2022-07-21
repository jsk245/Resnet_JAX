## Info
This is a recreation of the ResNet paper that can be viewed here: https://arxiv.org/abs/1512.03385. The ResNet-50 model was originally used to perform image classification, and it is a common model to copy weights from to use in other projects. The deepmind JAX-based haiku python library was used for recreation, and the model was trained using Google Colab. I trained the model for about 10 minutes on the cifar-100 dataset and managed to achieve 33% accuracy on the test set and 97% accuracy on the training set. \
\
Note: The model implemented here was the ResNet-50 model detailed in the figure of the paper which was made for ImageNet. Since cifar-100 images are 32x32 pixels and ImageNet images are usually preprocessed to be 256x256 pixels, the downsampling at the beginning of the implementation here is likely not optimal given the data.

## ToDo
- train model overnight to see how high the accuracy is afterwards
- take this model and train on ImageNet for comparison with the original paper
- fix excess RAM usage during training

### RAM usage
- I currently run into the issue described here where the memory is leaking somewhere: https://github.com/deepmind/dm-haiku/issues/340
- The current workaround is to pickle the model state/params and then load it again after resetting the runtime in Google Colab
