
# Goal-vs-Hole-v1: Gym Environment Conversion

## Overview

This project involves converting the **Non-gym “Goal-vs-Hole-v1” game** into a custom **Gymnasium** (formerly OpenAI Gym) environment. The task entails replicating the game's mechanics, defining action and observation spaces, and implementing intelligent agent training using reinforcement learning techniques.

## Game Description

- **Environment**: 4x4 grid.
- **Agent Actions**: `{Up, Down, Left, Right}`.
- **Start State**: Top-left corner.
- **Terminal States**: 
  - **Goal**: Grants a reward of `+100`.
  - **Holes**: Penalize with `-100`.
- **Non-Terminal States**: Reward `0`.
- **Objective**: Train an agent to maximize rewards by reaching the Goal while avoiding the Holes.

## Features

- **Custom Gym Environment**:
  - Action and state spaces defined.
  - Methods `step`, `reset`, and `render` implemented for seamless integration with Gymnasium workflows.
- **Agent Training**:
  - Tabular methods (e.g., dynamic programming) applied to optimize Bellman's equation.
  - Exploration-exploitation strategies incorporated with a discount factor `γ = 0.9`.
- **Visualization**:
  - Render multiple episodes as animated `.gif` files.
- **Configuration File** (Extra Credit):
  - Supports customizable parameters via an `env.ini` file (e.g., Hole/Goal positions, rewards, discount factors).

## Installation

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Run the custom environment:
   ```bash
   python run_goal_vs_hole.py
   ```

2. View rendered episodes:
   - Generated `.gif` files will be saved in the `renders/` directory.

## File Structure

- **`goal_vs_hole_env.py`**: Implementation of the custom Gymnasium environment.
- **`agent_training.py`**: Script for training the agent.
- **`env.ini`**: Configuration file for environment settings (optional).
- **`renders/`**: Directory to store `.gif` files of rendered episodes.
- **`requirements.txt`**: List of Python packages used in the project.
- **`README.md`**: This file.

## References

1. [Gymnasium Environment Creation](https://gymnasium.farama.org/tutorials/gymnasium_basics/environment_creation/)
2. [Custom Gym Environments - Towards Data Science](https://towardsdatascience.com/creating-a-custom-openai-gym-environment-for-stock-trading-be532be3910e)
3. [Non-gym Implementation Repository](https://github.com/ashiskb/RL-workspace)
