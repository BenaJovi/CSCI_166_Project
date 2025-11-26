# CSCI_166_Project
Deep Q-Learning on Atari game Ms-Pacman
Project is adapted from:https://github.com/everestso/summer25/blob/main/c166f25_02b_dqn_pong.ipynb

Deep Q-Learning on MsPacman
A comparison of DQN, Double DQN, and Dueling Double DQN
This project implements and compares three Deep Q-Learning architectures on the Atari game MsPacman using Gymnasium and PyTorch.
The goal is to evaluate how different Q-network and target-update strategies affect learning performance, stability, and gameplay behavior.

Overview We train three agents: 
Baseline DQN 
Standard convolutional Q-network
Experience replay 
Target network updates Epsilon-greedy exploration

Double DQN Uses online network for action selection 
Uses target network for Q-value estimation 
Reduces Q-value overestimation → more stable, slower early learning 

Dueling Double DQN 
Shared convolutional encoder 
Separate Value and Advantage streams 
Combines with Double DQN target selection 
Helps on games with state redundancy (but needs large training budgets) 

All three agents use the same preprocessing pipeline: 
AtariWrapper (grayscale, resize, frame-skip) 
Frame stacking (4 frames) 
Image→PyTorch channel reordering 
FIRE reset wrapper
