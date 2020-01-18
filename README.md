# PyTorch-Vanilla-DQN-Experiment
Experimenting with the effectiveness of Huber loss versus Mean Squared Error loss for a simple q-learner on the pole balancing problem. To toggle the loss function, simply adjust the value of mse in the hyperparameters section to true or false if you would like to use MSE loss or Huber loss respectively. Additionally, the amount of training episodes and number of experiments can be adjusted. The program runs the specified number of experiments, each with the specified number of episodes, then spits out the average performance of the agent throughout all experiments (it does become re-trained after each experiment).

When using the default hyperparameters and mean squared error loss, the agent achieved the following score over ten experiments with two hundred episodes each, with the graph illustrating performance of the final experiment:
![MSE_image](https://raw.githubusercontent.com/wfraher/PyTorch-Vanilla-DQN-Experiment/master/vanilla_dqn_mse.PNG)

On the other hand, doing the same thing with Huber loss achieved the following performance:
![Huber_image](https://raw.githubusercontent.com/wfraher/PyTorch-Vanilla-DQN-Experiment/master/vanilla_dqn_huber.PNG)

Interestingly, MSE loss outperformed Huber loss on this environment. Peculiarly, Huber is often regarded as more effective for Deep Q-Learning, which makes these results surprising. Perhaps playing around with the delta parameter for Huber loss would be better here, or MSE loss is intrinsically better for this environment for some reason. It is worth note that Huber loss appears to be more stable.
