# CSCI_166_Project MS. Pac-Man Double and Dueling DQN 
Deep Q-Learning on Atari game Ms-Pacman
This project explores Deep Reinforcement Learning methods by applying Double DQN and Dueling DQN to the Atari game Ms. Pac-Man. We benchmark these advanced variants against a standard DQN baseline to evaluate how architectural improvements influence learning dynamics and gameplay performance.

Project has been adapted from: https://github.com/everestso/summer25/blob/main/c166f25_02b_dqn_pong.ipynb


# Project Overview

We compare three Deep Q-Learning architectures on the ALE/MsPacman-v5 domain:

1. Baseline DQN: CNN-based Q-function approximator.

2. Double DQN: Uses online network for action selection and target network for evaluation to reduce overestimation.

3. Dueling DQN: Factorizes Q-values into Value and Advantage components for richer state evaluation.

Agents operate on 84×84 grayscale stacked frames (4 frames) and choose between 5 discrete actions.
The objective is to maximize cumulative reward by collecting pellets and avoiding enemy ghosts.
