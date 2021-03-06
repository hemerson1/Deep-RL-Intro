# Actor-Critic

## Project Summary:
- The homework topic was actor-critic algorithms. 
- In this project I implmented Proximal Policy Optimisation (PPO) to continuous action spaces. 
    - this model also used gradient clipping and generalised advantage estimation (GAE-$\lambda$)
- This project used OpenAI gym to make the environment cheetah 
    - to ensure the model was learning I tested it initially on LunarLander

## Files:
- Actor-Critic.ipynb - code for the PPO algorithm
- Images - training images
- Reward_Files - reward training data
- Models - training weights
    
## Training: 

### LunarLanderContinuous-v2

- The model took 1000 episodes to show that is was learning
- The model took approximately 5000 episodes to reach a mean score of greater than 200 required to 'beat' the environment. This equated to a couple of hours on cpu.
- I also measured the the performance of the model with respect to learning rate. The model appeared insensitive to order of 10 changes in learning rate.

Plot of Rewards       |  Gif of Final Product |  Learning Rate Comparison 
:-------------------------:|:-------------------------:|:-------------------------:
![](./Images/AC_Lunar_5000ep.png)  |  ![](./Images/AC_Lunar_5000ep.gif) |  ![](./Images/AC_Lunar_5000ep-lr_comp.png)

### HalfCheetah-v3

- The model took 1000 episodes to show that is was learning.
- The model took approximately 1000 episodes to reach a mean score of greater than 2700. This appears to be in excess of the benchmark using tensorflow for a PPO stated at: https://spinningup.openai.com/en/latest/spinningup/bench.html. 
- This took 1 hr of training to reach 1000 episodes on CPU. 
- I also measured the the performance of the model with respect to learning rate, lambda for the GAE and the batch size. 

Plot of Rewards       |  Gif of Final Product | 
:-------------------------:|:-------------------------:|
![](./Images/Cheetah_4000ep.png)  |  ![](./Images/AC_Cheetah.gif) | 


Batch Size Comparison     |  Lambda Comparison  |  Learning Rate Comparison 
:-------------------------:|:-------------------------:|:-------------------------:
![](./Images/Cheetah_1000ep-batch_comp.png)  |  ![](./Images/Cheetah_1000ep-lambda_comp.png) |  ![](./Images/Cheetah_1000ep-lr_comp.png)

## Extensions: 
- Implement A3C as this has been shown to be more efficient for CPU training: https://arxiv.org/pdf/1602.01783.pdf. 


## A Few Notes:
- Actor-Critic models are quick algorithms to run and achieve reasonable results, so perhaps worth considering for the final project. 