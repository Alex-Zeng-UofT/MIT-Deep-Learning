# Deep Generative Modeling

**Goal:**
> Take input training samples from some distribution and learn a model that represents that distribution capable of uncovering underlying features in a dataset

## Latent Variable Models

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/f3d94e45-f016-4256-9a34-0c21fcd7762c)

## Variational Autoencoders

### Autoencoders

> Unsupervised approach to learn low dimension feature representation of the unlabeled training data and can be trained to decode to a reconstructed obervation that resembles the original input

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/64bdc0a4-85cb-49fc-9a5a-4510cedf7a3c)

### Adding Variability

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/8b736c2c-a753-40ee-a993-64520f40046d)

### Loss Function = (Reconstructed Loss) + (Regularization Term)

Regularized Term measures the performance of the new inferred distribution relative to the prior

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/69a36483-e6ca-405b-9a19-ae3ffa227231)

### Regularization Should Achieve
1. Continuity: Points that are close in latent space should map to similar content after decoding
2. Completeness: Sampling from the latent space should yield semantically meaningful outputs

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/d50a4182-5f2a-465f-a434-b9cfc2fad280)

### Reparametrizing the sampling layer to allow for backpropagation

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/f810a105-3596-4f14-80bc-a7985431712b)

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/0cc49f7b-6396-4edb-97e4-bdbca79f818b)

### Latent Perturbation

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/4c4e9e14-b213-4cf9-bf73-9572a05e781f)

## Generative Adversarial Networks

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/7ebe61a4-1358-4416-8fbc-eddef3f1096e)

> GANs are distribution transformers

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/83200d30-c985-4ed9-aa46-9630a05e58ce)


### Paired GAN

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/404b4f44-c560-4df9-aa0f-51483834331e)

### CycleGAN: Domain Transformation

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/4f9c6a8d-6da7-45ac-8f3d-d697ee5b7dfd)

