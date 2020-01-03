# Robot-arm-reacher
Deep reinforcement learning agent that reaches an area in a unity environment. This project is the second graded project for the Deep Reinforcement Learning Nanodegree on Udacity.

A robotic double-jointed arm is trained to to reach an area defined in a green sphere. The agent is rewarded when it is contact with the goal sphere with a reward of +0.1 at each timestep.

The environment consists of a state space of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. The action space consists of a vector a vector with four numbers, corresponding to torque applicable to two joints. The environment is solved until the agent achieves a reward of at least +30.0 for 100 consecutive episodes.

I implemented a Deep Deterministic Policy Gradient approach (DDPG) because its advantages of combining policy and value based learning. 


[//]: # (Image References)
[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"

![Trained Agent][image1]

### Steps to get this thing going
1. Create a new environment with python version 3.6.x `conda create -n reacher python=3.6`
2. Activate your environment `conda activate reacher`
3. Install mlagents `pip install mlagents==0.4.0`
4. Install pytorch, get your command from https://pytorch.org/get-started/locally/ in my case it is `conda install pytorch torchvision cudatoolkit=10.1 -c pytorch`
5. Install jupyter lab (it looks good) `pip install jupyterlab`
6. Clone this repository `git clone https://github.com/juanluislopez24/robot-arm-reacher`
7. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

8. Uncompress the zip file on your desired folder

9. Open jupyter lab with `jupyter lab` and open the Navigation.ipynb file
10. Change the path for your unity environment on the cell that has `env = UnityEnvironment(file_name='env_v1/Reacher.exe')`
11. Run all the cells and train a new agent, or go down until the section of "Run the trained agent" and run all the remaining cells.


Have fun and thanks for passing through here!
