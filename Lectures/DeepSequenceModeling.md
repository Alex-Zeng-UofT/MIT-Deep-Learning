# Deep Sequence Modeling

## Applications and Scenarios

<img width="500" alt="1" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/8d6987c4-0256-41b8-89dc-9a91a9e662ec">


## Neurons with Recurrence

> Neurons that produces an output with a dependence on the previous/hidden state

<img width="401" alt="2" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/847f6146-954d-44a0-8354-b7436bb675b5"> <br/>

<img width="500" alt="Screenshot 2024-05-07 at 7 10 03 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/604eeb16-3911-4848-819c-22b1c64f7d13">

## Recurrent Neural Networks

> Apply a recurrence relation at every time step to process a sequence

<img width="500" alt="Screenshot 2024-05-07 at 7 13 08 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/5dc3dd6e-7a28-4ee8-add6-b3cc18ff8f0e">

### **Updating the state:**

> The output is calculated using the current state $h_t$ which is calculated using the hidden state $h_{t-1}$ and the current input $x_t$. The current state then becomes the hidden state for the next step in the sequence.

<img width="700" alt="Screenshot 2024-05-07 at 7 28 10 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/94da7564-f9ca-44dd-96e0-5d8a51f070a3">

## Design Criteria for Sequence Modeling

To model sequences, we need to be able to:

1. Handle **variable-length** sequences
2. Track **long term** dependencies
3. Maintain information about **order**
4. **Share parammeters** across the sequence

> Recurrent Neural Networks achieve these properties

## Backpropagation Through Time

<img width="930" alt="Screenshot 2024-05-07 at 8 01 27 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/febd849b-35a6-4e7f-9db3-4d7c9bf339d1">

### Computing the gradient with respect to $h_0$ involves many factors of $W_{hh}$ and repeated gradient computations

### Many values > 1 cause Exploding Gradients

**Mitigation**:
- Apply gradient clipping to scale big gradients

### Many values < 1 cause Vanishing Gradients, biases parameter to capture short term dependencies instead of long

**Mitigation**:
- Activation Functions: use ReLU to prevent f' from shrinking the gradient when x > 0
- Parameter Initialization: Initialize weights to identity matrix and biases to 0 to help prevent weights from shrinking to 0
- Gated Cells: use gates to add or remove information within each recurrent unit

## Limitations of Recurrent Neural Networks

1. Encoding bottleneck
2. Slow, no parellelization
3. Not long memory

## Attention is All You Need

**Intuition:** Attending the most important parts of an input

1. Identity which parts to attend to
2. Extract the features with high attention

### Learning Self Attention with Neural Networks

**Procedure:**
1. Encode **positional** information
   - Data is fed in all at once, use position-aware encoding
   <img width="300" alt="Screenshot 2024-05-07 at 8 27 08 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/985b5f69-7243-467b-922c-b729f3cef721">
2. Extract Query, Key, and Value for search

   <img width="300" alt="Screenshot 2024-05-07 at 8 30 52 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/95e3ab58-e21e-4884-802b-ea5a8f95b3ce">
3. Compute **attention weighting**
   - **Attention Score:** compute pairwise similarity between each query and key
   - Wrap **attention score** inside a softmax
   
   <img width="300" alt="Screenshot 2024-05-07 at 8 34 31 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/a19326a6-c277-4c4d-ab56-de0b7b1275d2"> <img width="305" alt="Screenshot 2024-05-07 at 8 46 02 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/6db99d4b-09d4-4ba0-83c6-7c74fe79493f">

4. Extract **features with high attention**

   <img width="300" alt="Screenshot 2024-05-07 at 8 47 43 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/69b06edf-6d79-46f5-b426-db0c68a86735">


> These operations form a self-attention head that can plug into a larger network. Each head attends to a different part of the an input.

<img width="574" alt="Screenshot 2024-05-07 at 8 51 08 PM" src="https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/0a2909bd-4907-4ce4-9306-d6d6c09a0704">


# Summary

1. RNNs are well suited for **sequence modeling** tasks
2. Model sequences via a **recurrence relation**
3. Training RNNs with **backpropagation through time**
4. Self-attention to model **sequences without recurrence**
5. Self-attention is the basis for many **large language models**
   

