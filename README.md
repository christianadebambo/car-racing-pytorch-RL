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
