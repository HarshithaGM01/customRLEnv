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


Experiment: Skill Amplification in Exploitation

I introduced an exploit_skill_multiplier parameter to test how strongly skill influences resource generation.
With the baseline multiplier (1.0), the agent preferred stable “safe” actions with minimal exploitation.
When the multiplier was increased (3.0), the agent shifted toward an exploit–rest cycle to maximize returns.
This demonstrates that environment transition dynamics can dominate reward shaping in driving policy behavior.
The experiment highlights how structural changes in state-action mechanics significantly alter learned strategies.
