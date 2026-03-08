# CartPole Deep Q-Learning Variants

This repository presents a reinforcement learning project on the **CartPole-v1** environment using **Deep Q-Learning (DQN)** in PyTorch.  
The project explores and compares multiple Q-learning architectures and training strategies, including baseline feedforward Q-networks, **target networks**, **Double DQN**, and **Dueling DQN**.

The workflow covers the full experimentation pipeline: model definition, agent training, performance evaluation, comparison across variants, checkpoint saving, and visual rollout rendering for trained agents.

## Project Highlights

- Implementation of several DQN-based agents in PyTorch
- Comparison of:
  - Small, medium, and large Q-networks
  - Target-network DQN
  - Double DQN
  - Dueling DQN
- Training on the `CartPole-v1` control task from Gymnasium
- Evaluation using average episodic reward over multiple runs
- Visualization of trained policies through rendered gameplay
- Support for loading and visualizing an external pretrained DQN model

## Repository Structure

```text
cartpole-dqn-variants/
├── dqn-cartpole-comparison.ipynb
├── README.md
├── requirements.txt
└── saved_models/            # generated after training
```

## Methods

The notebook defines multiple neural network architectures for approximating the action-value function:

- **Standard MLP Q-networks** with varying capacity
- **Dueling architecture** separating value and advantage estimation
- **Double DQN** to reduce overestimation bias
- **Target-network DQN** for more stable training

Training includes:
- epsilon-greedy exploration
- replay buffer sampling
- temporal-difference learning
- optional target network synchronization
- checkpoint saving for each trained variant

## Experimental Setup

- **Environment:** `CartPole-v1`
- **Framework:** PyTorch
- **RL paradigm:** value-based deep reinforcement learning
- **Evaluation metric:** mean episodic reward over multiple test episodes

The notebook compares learning curves and final evaluation performance across all configured agents.

## Installation

Create a virtual environment and install the dependencies:

```bash
pip install -r requirements.txt
```

If you are using Jupyter:

```bash
pip install notebook
jupyter notebook
```

## Usage

Open the notebook and run it cell by cell:

```bash
jupyter notebook code.ipynb
```

The notebook will:
1. define the Q-network variants,
2. train multiple CartPole agents,
3. save trained weights in `saved_models/`,
4. plot learning curves,
5. evaluate all trained models,
6. render policy rollouts as animations.

## Output

Typical outputs include:
- reward curves during training,
- a comparison table of mean and standard deviation of rewards,
- saved PyTorch checkpoints,
- rendered rollouts for trained policies.

## License

This project is shared as part of a personal machine learning and reinforcement learning portfolio.
