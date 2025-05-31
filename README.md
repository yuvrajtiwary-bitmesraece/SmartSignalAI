# SmartSignalAI

SmartSignalAI is a Reinforcement Learning-based intelligent traffic signal control system designed to optimize urban traffic flow. Built using SUMO (Simulation of Urban MObility) and Stable-Baselines3, the project trains and evaluates multiple RL agents—DQN, PPO, and A2C—to dynamically adjust traffic light phases in a simulated intersection. The objective is to minimize vehicle queue lengths and reduce overall waiting times through learned traffic signal policies.

This modular and extensible framework provides:
```
- A custom Gymnasium-compatible SUMO environment

- Training pipelines for different RL algorithms

- Performance evaluation and visualization tools for comparative analysis
```

## Features 

- Implements traffic signal control with 4 distinct phases representing main directions.
- Supports multiple RL algorithms: DQN, PPO, and A2C using Stable-Baselines3.
- Training pipeline with configurable timesteps and random seed control.
- Real-time environment interaction with step-wise state, reward, and done handling.
- Detailed reward calculation based on vehicle halting and queue length reduction.
- Comprehensive evaluation including cumulative reward and per-step reward analysis.
- Visualizations for reward trends, action distributions, and agent performance comparison.
- Efficient resource cleanup with proper SUMO session management and garbage collection.
- Modular code structure for easy extension and integration with other traffic scenarios.

## Tech Stack

1. **Python 3.8+** – Core programming language.
2. **SUMO (Simulation of Urban Mobility)** – Traffic simulation platform.
3. **Gymnasium** – Reinforcement Learning environment interface.
4. **Stable-Baselines3** – RL algorithms implementation (DQN, PPO, A2C).
5. **NumPy** – Numerical computations.
6. **Pandas** – Data handling and analysis.
7. **Matplotlib & Seaborn** – Data visualization and plotting.
8. **TRACI** – SUMO traffic control API for real-time interaction.
9. **Jupyter Notebook** – Development and experimentation environment.

## Folder Structure
```
SmartSignalAI/
│
├── Main Colab Notebook
├── Plots
├── requirements.txt
├── README.md
└── .gitignore

```

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the repository**
```
git clone https://github.com/yuvrajtiwary-bitmesraece/SmartSignalAI.git
cd SmartSignalAI
```

2. **Create and activate a virtual environment**
```
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

3. **Install required dependencies**
```
pip install -r requirements.txt
```

## How To Run?

You can explore the complete workflow (training + testing + visualization) using the Colab notebook: 

[Run on Colab](https://colab.research.google.com/drive/1ryY7hJGw-spLeHU-zbctgstVG_IEbkNe?usp=sharing)

## Result

This section presents the key visualizations that highlight the performance and behavior of the RL agents (DQN, PPO, A2C) trained for traffic signal control.

###  Reward Per Step (DQN Only)

Detailed reward trends step-wise specifically for the DQN agent to analyze its fine-grained performance.

![Reward Per Step DQN](https://raw.githubusercontent.com/yuvrajtiwary-bitmesraece/SmartSignalAI/main/Reward%20Per%20Step%20DQN.png)

###  Cumulative Reward Over Time (DQN Only)

Accumulated reward plot for DQN alone showing how rewards build up across simulation steps.

![Cumulative Reward Over Time DQN](https://raw.githubusercontent.com/yuvrajtiwary-bitmesraece/SmartSignalAI/main/Cumulative%20Reward%20Over%20Time%20DQN.png)

###  Action Distribution (DQN Only)

Phase choice distribution for DQN, highlighting its preferred traffic signal phases during the episode.

![DQN Action Distribution](https://raw.githubusercontent.com/yuvrajtiwary-bitmesraece/SmartSignalAI/main/DQN%20Action%20Distribution.png)

###  Cumulative Reward Over Time (DQN, PPO, A2C)

Displays the accumulated reward over the episode, indicating the total efficiency gain by each agent. Higher cumulative reward implies better traffic management.

![Cumulative Reward DQN PPO A2C](https://raw.githubusercontent.com/yuvrajtiwary-bitmesraece/SmartSignalAI/main/Cumulative%20Reward%20DQN%20PPO%20A2C.png)

###  Action Distribution (DQN, PPO, A2C)

Frequency of each traffic signal phase chosen by the agents. This helps understand policy preferences and traffic phase utilization.

![Action Distribution DQN PPO A2C](https://raw.githubusercontent.com/yuvrajtiwary-bitmesraece/SmartSignalAI/main/Action%20Distribution%20DQN%20PPO%20A2C.png)

###   Reward Per Step (DQN, PPO, A2C)

This plot shows the immediate reward received by each agent at every simulation step. It reflects how well each model reduces vehicle waiting times dynamically during traffic flow.

![Reward Per Step DQN PPO A2C](https://raw.githubusercontent.com/yuvrajtiwary-bitmesraece/SmartSignalAI/main/Reward%20Per%20Step%20DQN%20PPO%20A2C.png)

## Thank You

Grateful for your time and attention — it truly means a lot!
