
### DQN:
---

Deep Q learning algorithm uses learned neural networks weights to represent action-values instead of using fixed table to store values for each action. This is particularly useful to deal with the complexity of large observation space like raw images. Neural networks work as non-linear function approximators to calculate the value of actions based on observation form the environment.For example going from pixels to best actions to maximaise reward. This results in intuitive, human like behavior and gives RL agents way to make sense of the environment.

DQN uses two separate neural networks with identical architecture, one serves as a temporary fixed target and the other one constantly update its weights.

#### Two tecniques were implemented in this project:

1 - Use of rolling history of past experiences by using a reply pool. the behvior distribution is averaged over many of its previous states, to smooth out learning and avoid oscillation. That results in each step in the experience to be used in many weight updates, which allows for further optimisation if we want to prioritise rare events and make sure that we always take them into consideration when we update the network weights. Using experience replay also helps breaking harmful correlation between consequetive experiences.

2- Target Network: used to compute the loss of each batch of actions during training.

#### Hyperparameters
Hyperparameters used to obtain final resutls:
```
BUFFER_SIZE = int(1e5)  # replay buffer size
BATCH_SIZE = 64         # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR = 5e-4               # learning rate 
UPDATE_EVERY = 4        # how often to update the network
```

### Results
---
The agent reach the goal of collecting average reward of 13 over 100 episodes after 535 training episodes.

[image1]: assets/results.png "results"

![results][image1]

#### Future work
--- 

Implement the following algorithm:
- Prioritized experience replay
- Dueling DQN
- Rainbow

References:  
- Riedmiller, Martin. "Neural fitted Q iteration–first experiences with a data efficient neural reinforcement learning method." European Conference on Machine Learning. Springer, Berlin, Heidelberg, 2005. http://ml.informatik.uni-freiburg.de/former/_media/publications/rieecml05.pdf

- Mnih, Volodymyr, et al. "Human-level control through deep reinforcement learning." Nature518.7540 (2015): 529. http://www.davidqiu.com:8888/research/nature14236.pdf
