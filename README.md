# ExchangeAgent

Training a stock exchange agent with Reinforcement Learning algorithms and Decision Transformer.

> Environment

- The environment used was the `gym-anytrading`, which can load stock exchange history as an OpenAI Gymnasium environment, and enable users to train their custom agents to trade stocks in the environment.
- The environment returns a window of stock exchange prices as the observation and allows for action `0` for selling the stocks and `1` for buying the stocks.

> Reinforcement Learning Algorithms

- The first set of agents was trained using A2C and PPO algorithms implemented in the `stable-baselines3` library.
- The agents were trained on each algorithm with 25K, 50K, 100K, 200K, 500K, and 1M timesteps.
- The best-performing agent was the PPO algorithm with 200K timesteps, which collects around ~900 avg. reward on an episode.

Performance Comparison between Models:
<p align="center">
  <img src="./data/random-a2c-25-50-100-steps-comparison-chart.png" alt="random-a2c-25-50-100-steps-comparison-chart.png" width="500"/>
  <img src="./data/random-a2c-200-500-1000-steps-comparison-chart.png" alt="random-a2c-200-500-1000-steps-comparison-chart.png" width="500"/>
</p>
<p align="center">
  <img src="./data/random-ppo-25-50-100-steps-comparison-chart.png" alt="random-ppo-25-50-100-steps-comparison-chart.png" width="500"/>
  <img src="./data/random-ppo-200-500-1000-steps-comparison-chart.png" alt="random-ppo-200-500-1000-steps-comparison-chart.png" width="500"/>
</p>

> Decision Transformer
