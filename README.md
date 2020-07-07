[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/43851646-d899bf20-9b00-11e8-858c-29b5c2c94ccc.png "Crawler"


# Project 2: Continuous Control

### Project Details

For this project, we will work with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

#### Distributed Training

For this project, I have used an environment that contains 20 identical agents, each with its own copy of the environment.  

This version is useful for algorithms like [PPO](https://arxiv.org/pdf/1707.06347.pdf), [A3C](https://arxiv.org/pdf/1602.01783.pdf), and [D4PG](https://openreview.net/pdf?id=SyZipzbCb) that use multiple (non-interacting, parallel) copies of the same agent to distribute the task of gathering experience. 

### Getting Started
1. Install anaconda on __Windows__ using windows installer at https://www.anaconda.com/products/individual#windows

2. Create (and activate) a new environment with Python 3.6.
    - __Windows__: 
    ```bash
    conda create --name drl python=3.6 
    activate drl
    ```
    
3. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/KanikaGera/Navigation-Game-RL.git
cd setup 
conda install pytorch=0.4.1 cuda90 -c pytorch
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drl` environment.  
```bash
python -m ipykernel install --user --name drl --display-name "drl"
```

5. Before running code in a notebook, change the kernel to match the `drl` environment by using the drop-down `Kernel` menu. 

### Structure of Repository
1. `Continous_Control.ipynb`  consist of unityagent ml library to interact with unity environment and train the agent.
    
2. `model.py` consists of structure of RL model coded in pytorch.
    
3. `ddpg_agent.py` consist of DDPG Algorithm Implementation .
    
4. `checkpoint_actor.pth`  is saved trained model with weights for actor network.

5. `checkpoint_critic.pth`  is saved trained model with weights for critic network.

### Instructions
1. Install Dependies by following commands in __Getting Started__
    
2. Download the environment from one of the links below.  You need only select the environment that matches your operating system:

    - **Twenty (20) Agents_**
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

   
3. Place the file in the GitHub repository, in the main folder, and unzip (or decompress) the file. 

#### Train The Agent
4. Open Continous_Control.ipynb 
5. Run Jupyter Notebook 
6. Run the cells to train the model.

