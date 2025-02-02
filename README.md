Here's an enhanced version of the README for your project:

---

# Task Offloading in Edge Devices using Reinforcement Learning

## Project Description

This project addresses the challenge of **task offloading in edge computing devices**. It simulates a scenario where tasks arrive with specific time stamps and need to be processed within a certain time window. The goal is to optimize task offloading decisions using **Reinforcement Learning (RL)** techniques, specifically the **Double Q-Learning** model. 

In the simulation, both **edge devices** and **node devices** participate in processing tasks. The RL model observes the current state and minimizes Q-values to make offloading decisions, determining whether tasks should be processed locally on the edge device, offloaded to a node device, or dropped based on resource availability and task requirements.

## Features

- **Task Generation**: Tasks are generated with unique IDs and random time stamps.
- **Task Offloading**: Tasks are pushed to edge nodes, where the RL model calculates load and makes offloading decisions.
- **FIFO Queueing**: Both edge and node devices use FIFO (First In, First Out) queues to manage task processing.
- **Reinforcement Learning Model**: The task offloading decision is made by the RL model, observing the system's state and minimizing Q-values.
- **Task Processing Strategies**: Tasks are either processed locally, offloaded to a node device, or dropped based on the optimal decision from the model.

## Installation

To get started with the project, follow these steps:

1. **Clone the Repository**

   Clone the repository to your local machine:

   ```bash
   git clone git@github.com:abhishekprakash256/deep-learning-in-edge-computing.git
   ```

2. **Navigate to the Project Directory**

   Change to the project directory:

   ```bash
   cd Deep_learning_in_edge_computing/
   ```

3. **Install Dependencies**

   Install the required dependencies by using the `requirements.txt` file:

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Simulation**

   Navigate to the `files/` directory and run the simulation script:

   ```bash
   cd files/
   python3 exp_19.py
   ```

## Dependencies

The project relies on the following dependencies. Ensure that they are installed:

- Python 3.x
- `numpy`
- `tensorflow`
- `keras`
- `matplotlib`
- Any other dependencies mentioned in the `requirements.txt` file.

For a full list of dependencies, please refer to the `requirements.txt` file.

## Steps

Here’s a brief breakdown of how the task offloading and RL model work:

1. **Task Generation**: Tasks are generated using a random function with unique IDs and time stamps.
   
2. **Task Offloading to Edge Nodes**: Tasks are pushed to the edge node devices. The load on each device is calculated.

3. **Load Calculation and Model Input**: The calculated loads (resource requirements) are fed as input to the Deep Q-Learning model.

4. **Task Queuing**: Both edge and node devices maintain a queue (FIFO) to store tasks that need to be processed.

5. **State Observation and Decision Making**: The RL model observes the current system state and calculates the optimal task processing strategy. The decision is based on minimizing the Q-values, which reflect the optimal strategy for task offloading.

6. **Offloading Decision**: Based on the decision from the model, the task is either:
   - Processed locally on the edge device.
   - Offloaded to a node device.
   - Dropped if there are insufficient resources.

## Files Directory

The `files/` directory contains the necessary files for the simulation, including:

- **exp_18.py**: Experimental setup and code for a variant of the model.
- **exp_19.py**: Main simulation script for task offloading using Double Q-Learning.
- **dueling_q_model.py**: The implementation of the Dueling Q-Learning model used for task offloading decision making.

## Notes

- The task processing is performed using **FIFO queues** for both edge and node devices.
- The RL model observes the state space and makes decisions based on the load calculations from the edge and node devices.
- The project utilizes the **Double Q-Learning model** to optimize task offloading.
- The model ensures efficient task processing by minimizing Q-values based on the current state.

## Illustration

![Task Offloading Flow](path_to_your_image.png)

## Future Work

- **Scalability**: Extend the model to support more devices and tasks.
- **Improved Algorithms**: Experiment with other reinforcement learning algorithms like Proximal Policy Optimization (PPO) or A3C.
- **Real-World Integration**: Implement the model in real-world edge computing environments to validate its performance.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This enhanced version of the README provides a clearer explanation of the project, instructions on how to set it up, and additional context for the model and its functionality. Let me know if you need further modifications!
