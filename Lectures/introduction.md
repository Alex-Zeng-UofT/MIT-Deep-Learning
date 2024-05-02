# Introduction

## Why Deep Learning and Why Now?

### Why Deep Learning?
> Hand engineered features are time consuming, brittle, and not scalable in practice. 

- We can learn the underlying features directly from data!

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/4a1e8e60-e418-428d-b12f-218525c5f0e7)


### Why Now?

> Neural Networks data back decades, so why the dominace now?

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/3db95df8-ec2c-4f27-970f-91ff77e68aab)

**Today, we have the resources**
1. Big Data
   - Larger datasets
   - Easier collection and storage
2. Hardware
   - GPUs
   - Massively parallelizable
3. Software
   - Improved techniques
   - New models
   - Toolboxes

## The Perceptron/Neuron : Forward Propagation

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/3b323bf1-841a-4a88-adf6-3154a425d16e)

### Activation Functions: a non-linear function

**Purpose**: to introduce non-linearity into the network

> Some common activation functions:

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/b33940e1-6837-4be5-8af5-0e00d00a09dc)


## Building Neural Networks with Perceptrons

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/8d484b29-5a4e-47eb-a493-24083a060780)

## Loss and Cost

The **loss** of out network measures the cost incurred from incorrect predictions

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/41c25cff-c19a-4361-b87b-b81c899a8b18)

### Empirical Loss

The **empirical loss** measures the total loss over the entire dataset

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/f6b3b84a-0d31-4445-9608-7e5418f5be05)

### Binary Cross Entropy Loss

**Cross entropy loss** can be used with models that output a probability between 0 and 1

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/369284a5-7cc9-4bb0-9c8c-96ad2033d143)

### Mean Square Error Loss

**Mean squared error loss** can be used with regression models that outputs continuous real numbers

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/2cc62254-2bcf-4ab2-947e-e6fa95884359)

## Training Neural Networks

### Loss Optimization

We want to find the network weights that achieve the lowest loss

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/90bc3657-f5e2-4186-970d-86ede54b40e0)

### Gradient Descent

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/5d5ca197-bbdc-4d81-a7bc-8dbc2586c7c8)

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/4371309e-01e4-40d0-a754-3395b7c4211b)

**Algorithms**

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/2539d502-f31a-470b-9201-833d98d80579)

## Back Propagation

Used to compute gradient sequentially backwards starting from output layer

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/7a290c8d-01c6-4764-8980-611741d01062)

## In Practice

Training neural networks is difficult, loss functions can be difficult to optimize

How do we set a learning rate so it doesn't:
1. Converge slowly and get stuck at false local minima (Small Learning Rate)
2. Overshoot and become unstable and diverge (Large Learning Rate)

Ideas:
1. Brute force the learning rate (Not Practical)
2. Adaptive learning rates (Bingo)

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/b8bd7034-ee8e-44e0-96a7-3a9c6f03826a)

### Batching 

Mini batches for training allows for higher training rates, smoother convergence, and increased accuracy of estimated gradient

**Stochastic Gradient Descent**

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/c8fcc7cf-8875-494b-921f-94c5171ec8d5)

## Overfitting

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/f2eada2e-c9fd-4dc3-9232-cfd89919a1ef)

**Regularization**
- Constrains optimization problem to discourage complex models
- Improve generalization on unseen data

Techniques
1. Dropout

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/3ae3f9b2-c0a5-4db7-afe6-ca453651b89a)

2. Early Stopping

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/c8a0f999-5f8b-4f8b-b1e7-226891019e6d)


# Review

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/e4bdbdd6-34af-4991-a0c1-9ac0a5cc512c)
