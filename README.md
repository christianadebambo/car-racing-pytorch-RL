# Proximal Policy Optimization (PPO) for CarRacing-v0

This repository contains an implementation of the Proximal Policy Optimization (PPO) algorithm for training an agent to play the CarRacing-v0 game from the OpenAI Gym environment. The agent learns to navigate a racing track using a neural network-based policy and value function estimation.

## Requirements

- Python 3+
- PyTorch
- NumPy
- Gym
- Argparse

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
