# Proximal Policy Optimization (PPO) for CarRacing-v0

This project contains an implementation of the Proximal Policy Optimization (PPO) algorithm for training an agent to play the CarRacing-v0 game from the OpenAI Gym environment. The agent learns to navigate a racing track using a neural network-based policy and value function estimation.

## Requirements

- Python 3+
- PyTorch
- NumPy
- Gym
- Argparse

## Project Structure

The repository consists of the following files:

- `train.py`: The script for training the PPO agent on the CarRacing-v0 environment.
- `test.py`: The script for testing the trained agent on the CarRacing-v0 environment.
- `utils.py`: Utility module containing a class for visualization using Visdom.
- `param/ppo_net_params.pkl`: Saved model parameters for the trained PPO agent.

## Code Overview

- `train.py`: This script is responsible for training the PPO agent. It takes command-line arguments to customize the training parameters, such as the discount factor, action repeat, image stack size, random seed, rendering option, visualization option, and log interval. The PPO algorithm is implemented using a neural network model for the actor-critic architecture. The training loop runs for a specified number of episodes, during which the agent interacts with the environment, selects actions based on the policy, and updates the model using the PPO algorithm. The moving averaged episode rewards are visualized using the Visdom library if the visualization option is enabled. The trained model parameters are saved in param/ppo_net_params.pkl.
  
- `test.py`: This script is used to test the trained PPO agent on the CarRacing-v0 environment. It takes command-line arguments similar to train.py, such as the action repeat, image stack size, random seed, and rendering option. The agent's trained model parameters are loaded, and the agent interacts with the environment using the learned policy. The episode scores are printed to evaluate the agent's performance.
  
- `utils.py`: This module contains a utility class called DrawLine. It utilizes the Visdom library to provide a simple way to plot and visualize data using line graphs. The DrawLine class is used in train.py to visualize the moving averaged episode rewards during training.

## Installation

Clone the repository:

   ```shell
   git clone https://github.com/christianadebambo/car-racing-pytorch-RL.git
   ```

## Usage

1. Set up Visdom server:

Before training with visualization, start a Visdom server by running the following command:

   ```shell
   python -m visdom.server
   ```

2. Training and Testing:

To train the agent, run ```python train.py --render --vis``` or ```python train.py --render``` without visdom. 

To test, run ```python test.py --render```.
