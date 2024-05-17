# Deep Computer Vision

## What a Computer Sees

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/0b896a9c-817d-4624-8485-861de529fbc4)

## Learning Visual Features

Converting an image to oen dimension vector and processing it with a traditional fully connected neural network is not feasible due to loss of the spacial and geometrical respresentation of the image

### Convolution

> Use convolution to first iteratively process and compress the image before sending it off to a fully connected neural network

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/af8d631c-0b52-4f8c-9cd3-7718a9d167bb)

### Procedure:
1. Element wise multiply the filter with a space
2. Sum up the products to yield a measurement for that space

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/5fbb2bd4-4ef5-4f58-93e8-8e66ac2f0d3f)


## Convolution Neural Networks for Classification

1. **Convolution**: Apply filters to generate feature maps
2. **Non-linear**: Apply a non-linear transformation, often ReLU
3. **Pooling**: Downsampling operation on each feature map

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/213839fc-d83a-486d-851b-8d4a9a0a1a77)

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/fe648fc6-39f8-4eb2-b8ab-12374057ba89)

