# Reinforcement Learning

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/75635303-55a4-47d8-aebe-5c19d520e93a)

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/420f64cb-c45a-48b7-a520-e8923b287c20)


## Key Concepts

**Agent:** Takes action and observes environment

**Action:** A move that an agent applies to an environment

**Observations:** Effects in environment after applying actions

**Rewards:** Feedback that measures success or failure of agent's action

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/34464161-a928-41fb-b769-68cdadaec723)

**Total Discounted Rewards:** ![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/b54f031f-c168-44c4-b4a7-b280e4da1650)

## The Q Function

> Captures the expected total future reward an agent in state s can receive by executing a certain action a

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/94d658fe-45e1-4ec4-b252-bfd8c55ff322)

## Policy $\pi(s)$

> Used to infer the best action to take at state s

**Strategy:** the policy should choose an action that maximizes future reward

## Value Learning

**Procedure**:
1. Find Q(s, a)
2. select action a such that a = argmax(s, a) holding s constant

### Deep Q Networks 

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/edd776e8-f52c-4937-a1a2-0e8af692bce3)

> Taking all the best actions result in a minimum Q-Loss

**Downsides:**
1. Cannot handle continuous action spaces due to complexity
2. Cannot learn stochastic policies due to deterministic computations

## Policy Learning

> Sample directly from distribution to stochastically get a valid action

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/03d8bebe-c6e8-4965-9cba-6b63209adf58)

**Allow for continuous sampling due to continuous distribution**

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/72328347-211a-4a33-be43-8f8b75be1e51)

### Training Algorthim
1. Initialize the agent
2. Run a policy until termination
3. Record all states, actions, rewards
4. Decrease probability of actions that resulted in low rewards
5. Increase probability of actions that resulted in high rewards

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/9f56aead-5022-4d09-a899-d286ca48d4f5)

# Summary

![image](https://github.com/Alex-Zeng-UofT/MIT-Deep-Learning/assets/114100209/8c93bab8-d9c7-41ca-a08d-a85c14d35e22)


