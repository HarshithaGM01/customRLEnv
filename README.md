# customRLEnv
# Long Horizon RL Environment

A custom reinforcement learning environment modeling long-term decision making under uncertainty.

## Motivation
Most RL tutorials focus on short-term reward optimization.
This environment studies delayed rewards, burnout dynamics,
risk-taking, and long-term stability.

## State Space
[skill, energy, resources, confidence, market_noise]

All values normalized to [0, 1].

## Actions
0 - Invest in skill  
1 - Exploit skill  
2 - Rest  
3 - Risky opportunity  
4 - Play safe  

## Reward Design
reward = growth_reward - burnout_penalty + immediate_signal

Optional skill bonus parameter enables reward sensitivity experiments.

## Experiments
- PPO vs Random baseline
- Reward sensitivity analysis
- Action distribution analysis
