# Report
### Learning Algorithm
I implemented DDPG. I chose ddpg because of its faster convergance. I took the base from the bipedal agent provided by Udacity, and adapted it for this project. Added an epsilon parameter for the OUnoise, because the agent was not learning. 

The hyperparameters I chose are:
- BUFFER_SIZE = 100000  
- BATCH_SIZE = 128   
- GAMMA = 0.99       
- TAU = 1e-3      
- LR_ACTOR = 0.0004      
- LR_CRITIC = 0.0004     
- WEIGHT_DECAY = 0.0001 
- UPDATE_EVERY = 10
- UPDATE_NUM = 4
- EPSILON = 1.0
- EPS_DECAY = 0.00005
- EPS_END=0.03

I trained the agent for 2000 episodes, reaching an average score of 33.69 through the last 100 episodes. The agent learned very fast, but was not as consistent. The agent obtained a reward of +30.0 around episode 500 of training, and after that it remained around +28.0 up to 38.0 thorugh the remaining episodes. 


### Plot of Rewards 
[image1]: scores.PNG "rewards"
![Rewards][image1]

 

### Ideas for Future Work
This is the most basic implementation of a ddpg agent. An idea for improvement would be to first to create an agent that could use the advantage of distributed learning with the 20 agent version. D4PG could be implemented, where we can train multiple agents in parallel. A distributed critic is introduced, if we improve how our critic estimates then the actor will improve, because it relies on it. N-step return could also be implemented so the value estimated could be more precise. Priority sampling, so the agent could learn the most.

