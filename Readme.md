
[image1]: assets/Banana_collecter.gif "Trained Agent"



### Introduction
---


![Trained Agent][image1]


This is an excercise to train an RL agent using DQN to navigate (and collect bananas!) in a large, square world. This is a customised version of [Banana Collecter](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#banana-collector) from Unity ML agents.

### The agent 
---

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. 


## State and Action Space
---
Four discrete actions are available, corresponding to:
- `0` - walk forward 
- `1` - walk backward
- `2` - turn left
- `3` - turn right      
        
This is an episodic task, in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.




## Running the code:
--- 
1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Install dependencies from `requirements.txt` file using:     
```
pip3 install -r requirements.txt
```
3. Place the file inside the main folder of this repository, and unzip (or decompress) the file. 

4. Run `Navigation.ipynb` to train the agent then use the provided function to watch trained agent navigating the Banana environment!

## License

DQN_Navigator is released under the MIT license. See [LICENSE](https://github.com/amrakm/DQN_Navigator/blob/master/LICENS) for more information.
