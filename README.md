# Joshua

“**Shall we play a game?**”

Welcome to **Joshua**, a multi-agent reinforcement learning project, the name is inspired by the classic film *WarGames* a firm favourite from the authors childhood years. Just as Joshua, the computer in *WarGames*, was designed to simulate complex strategic scenarios, this repository brings together path planning, intercept calculations, and decentralised multi-agent reinforcement learning (MARL) to create sophisticated simulations of cooperative and competitive interactions.

In *Joshua*, agents learn to move, communicate, and coordinate as they take on challenging tasks, from escorting targets to intercepting adversaries. With each layer, we dive deeper into the evolution of multi-agent systems, empowering each agent with the ability to make independent, intelligent decisions.

**joshua:$ [y/n]: y**

# Multi-Agent Path Planning and MARL for Cooperative and Competitive Scenarios

This project is an exploration of multi-agent systems, path planning, and reinforcement learning, culminating in a decentralised multi-agent reinforcement learning (MARL) system. Each step in this project builds on the previous one, progressively moving from simple path generation to complex MARL training for cooperative and competitive scenarios. 

## Table of Contents
1. [Overview](#overview)
2. [Basic Path Generation](#basic-path-generation)
3. [Intercept Calculations](#intercept-calculations)
4. [Introduction to Reinforcement Learning](#introduction-to-reinforcement-learning)
5. [Multi-Agent Scenarios and Communication](#multi-agent-scenarios-and-communication)
6. [Decentralised Multi-Agent Reinforcement Learning (MARL)](#decentralised-multi-agent-reinforcement-learning-marl)

---

## Overview

This project demonstrates how to design and train agents for complex scenarios, such as an escort mission or intercepting a target, by combining classic path-planning algorithms with modern reinforcement learning techniques. Starting from basic geospatial calculations, we gradually introduce reinforcement learning and decentralised multi-agent systems to equip each agent with the capability to make independent decisions, communicate with others, and adapt to dynamic environments. 

## 1. Basic Path Generation

The foundation of this project starts with generating basic paths for individual agents, such as people, drones, or vehicles. This step uses Python to create paths based on waypoints, speed, and direction. The goal is to build a path generator that respects speed limits and provides realistic movement patterns for agents. These generated paths can be used as a base for testing intercept and escort strategies.

**Key Concepts:**
- Generate paths for different entities based on waypoints and average speed.
- Ensure smooth transitions between waypoints and realistic movement within speed constraints.

This basic setup allowss the simulation of straightforward movement, serving as a basis for further complexity in path planning.

## 2. Intercept Calculations

Building on the path generator, we introduce **intercept calculations** to simulate scenarios where one agent (e.g., a drone) tries to intercept another moving agent (e.g., a person or vehicle). Geospatial libraries arr used to compute bearings and distances, enabling the intercepting agent to adjust its course dynamically based on the target’s position.

**Key Concepts:**
- Calculate the bearing and distance between two moving entities.
- Enable dynamic path adjustments based on real-time location updates.
- Develop basic collision-avoidance logic.

This intercept system introduces agents’ interactions with each other, laying the groundwork for competitive or cooperative behavior.

## 3. Introduction to Reinforcement Learning

With paths and intercept logic in place, the project then incorporates **reinforcement learning (RL)** to allow agents to learn optimal behaviors over time. Using Gym environments and a reinforcement learning framework like `stable-baselines3`, a single agent is trained (e.g., a helicopter) to complete a task, such as escorting another moving entity (e.g., a ship).

**Key Concepts:**
- Set up a Gym environment to simulate scenarios for an agent.
- Use an RL algorithm (such as PPO) to train the agent based on reward feedback.
- Define reward structures that encourage desirable behaviors (e.g., staying close to the escorted entity).

This step introduces the concept of **learning from experience**, allowing agents to improve their performance by maximising cumulative rewards over time.

## 4. Multi-Agent Scenarios and Communication

As we progress, we expand to **multi-agent scenarios**, where multiple agents interact within the same environment. These scenarios can be cooperative (e.g., multiple agents working together to escort a target) or competitive (e.g., one agent intercepting another). 

We also introduce **limited communication** between agents, enabling them to share information about their positions or intentions. This communication is crucial for multi-agent coordination, allowing agents to avoid conflicts and make better decisions without centralised control.

**Key Concepts:**
- Extend the environment to support multiple agents interacting in the same space.
- Design a communication protocol to allow agents to share information without centralised control.
- Implement cooperative and competitive strategies based on shared or conflicting goals.

Communication adds a layer of complexity, where agents learn to coordinate actions, enhance efficiency, and adapt to each other's strategies.

## 5. Decentralized Multi-Agent Reinforcement Learning (MARL)

Finally, all the components are brought together into a **decentralized multi-agent reinforcement learning (MARL)** framework. Each agent independently learns a policy to optimize its objectives, but they must rely on limited communication and observation of their surroundings. Using algorithms suited for MARL, such as **Multi-Agent Proximal Policy Optimisation (MAPPO)**, allowing agents to learn from each other while remaining decentralised.

**Key Concepts:**
- Implement decentralised training where agents learn independently without a central controller.
- Utilize MARL algorithms that support both cooperative and competitive dynamics.
- Train agents to handle complex tasks that involve multi-agent coordination, such as escorting, interception, and evasion.

Decentralised MARL allows agents to operate independently and scale more effectively, making the system robust for real-world applications where centralised control may be impractical or impossible.

---

## Getting Started

Each folder in this repository corresponds to one of the stages described above. Start by exploring the `path_generation` and `intercept_calculations` folders to understand the foundation, then proceed to `single_agent_rl`, `multi_agent_scenarios`, and finally `decentralized_marl`.

### Running the Code
- **Path Generation**: Run the Python scripts in the `path_generation` folder to generate basic paths for single agents.
- **Intercept Calculations**: Use the scripts in the `intercept_calculations` folder to simulate intercept scenarios.
- **Reinforcement Learning**: Train a single agent using the `single_agent_rl` folder and observe how it learns to escort or intercept.
- **Multi-Agent Scenarios**: Run the examples in `multi_agent_scenarios` to see multiple agents interact and communicate.
- **Decentralised MARL**: Use `decentralised_marl` to train multiple agents simultaneously in cooperative and competitive tasks.

### Outputs
Each stage has the option to output to either CoTs or for a quicker and historical feedback, plotly.

---

This project is designed to be exploratory, with the aim of gaining a solid understanding of MARL and how to build scalable, decentralised, and cooperative multi-agent systems.

Happy experimenting!
