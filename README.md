# Traffic Light Optimization Using Reinforcement Learning

This project presents a robust framework for optimizing traffic flow at complex intersections using a Deep Q-Learning Reinforcement Learning agent. By intelligently determining optimal traffic light phases, the agent continuously learns to maximize intersection throughput and minimize vehicle waiting times.

---
## Deep Q-Learning Agent
### Framework: Q-Learning enhanced with a deep neural network for function approximation.
### Context: Autonomous traffic signal control at a single urban intersection.
### Environment: Simulates a 4-way intersection with 4 incoming and outgoing lanes per arm, each stretching 750 meters. Traffic lights are configured so that each arm supports dedicated movement lanes (left, straight, right).
### Traffic Generation: Each training episode spawns 1000 vehicles following a randomized dynamic pattern, simulating realistic and varied traffic conditions.
### Agent: Traffic Signal Control System - TLCS
### State: A discretized snapshot of oncoming lanes, encoding vehicle presence across fixed-length cells.
### Action: Selection among predefined traffic light phase configurations, with each phase lasting 10 seconds.
### Reward: Computed based on the reduction in cumulative vehicle waiting time, encouraging the agent to clear congestion efficiently.
### Learning Mechanism: Employs the Q-learning update rule combined with a deep neural network to approximate state-action value functions and iteratively refine the agent's decision-making policy.

---
# Getting Started

## Follow the steps below to set up and run the project on your local machine:
### Download and install Anaconda from the [official website](https://www.anaconda.com/download?utm_source=chatgpt.com).
### Download and install SUMO from the [official website](https://sumo.dlr.de/docs/Downloads.php?utm_source=chatgpt.com).
### Ensure your environment satisfies the following software version requirements:
#### Python 3.11
#### SUMO traffic simulator 1.2.0
#### tensorflow 2.16.1
#### tensorflow-gpu 2.5.0
#### matplotlib 3.6.0
#### numpy 1.19.5

## Running the Algorithm
### Clone or download this repository.
### Open a terminal and navigate to the root project folder.
### Execute python training_main.py to begin the training process.

## Code Structure
### The codebase is organized into distinct classes, each responsible for a specific aspect of the training pipeline:
### Model: Defines and initializes the deep neural network architecture used by the agent.
### Memory: Implements experience replay, storing past transitions to improve training stability and sample efficiency.
### Simulation: Manages the simulation lifecycle, including interaction with the SUMO traffic simulator.
### TrafficGenerator: Handles the procedural generation of vehicle routes for each training episode.
### Visualization: Provides utility functions for rendering training metrics and performance plots.
### Utils: Contains helper functions for directory management, file I/O, and configuration parsing.

## Settings Explained
### All training and testing hyperparameters are stored in training_settings.ini and testing_settings.ini. 
### These configuration files control key parameters such as episode duration, traffic volume, neural network architecture (layer sizes, learning rate), and simulator-specific settings.

---
# Contributors
## This project was developed by:
#### Shubham Gusain
#### Harsh Gupta
#### Priyansh Kisan

### For questions, suggestions, or bug reports, please open an issue on the repository's issues page.

---
# References
### 1. V. Mnih et al., "Human-level control through deep reinforcement learning," Nature, vol. 518, pp. 529-533, 2015. 
### 2. L. El-Tantawy, B. Abdulhai, and H. Abdelgawad, "Multiagent Reinforcement Learning for Integrated Network of Adaptive Traffic Signal Controllers (MARLIN-ATSC)," IEEE Transactions on Intelligent Transportation Systems, vol. 14, no. 3, pp. 11401150, 2013. 
### 3. M. Wiering, "Multi-Agent Reinforcement Learning for Traffic Light Control," Proceedings of the Seventeenth International Conference on Machine Learning (ICML), 2000. 
### 4. P. Alvarez Lopez et al., "Microscopic Traffic Simulation using SUMO," Proceedings of the 21st International Conference on Intelligent Transportation Systems (ITSC), IEEE, 2018.
### 5. A. Casas, "Deep Reinforcement Learning for Traffic Signal Control," Stanford University CS229 Project Report, 2017. 
### 6. S. El-Tantawy and B. Abdulhai, "Towards Multi-Agent Reinforcement Learning for Integrated Network of Adaptive Traffic Signal Controllers," Proceedings of the 13th International IEEE Conference on Intelligent Transportation Systems, 2010. 
### 7. SUMO Documentation — Simulation of Urban MObility, https://sumo.dlr.de/docs/, accessed April 2026. 
### 8. OpenAI Gym Documentation, https://gymnasium.farama.org/, accessed April 2026. 
### 9. TensorFlow Documentation, https://www.tensorflow.org/api_docs, accessed April 2026.
### 10. PyTorch Documentation, https://pytorch.org/docs/, accessed April 2026. 
### 11. R. Sutton and A. Barto, Reinforcement Learning: An Introduction, 2nd ed. Cambridge, MA: MIT Press, 2018. 
