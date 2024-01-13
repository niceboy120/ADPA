# Adaptive Decentralized Policies with Attention (ADPA) (Still in Dev)

## Overview
The Adaptive Decentralized Policy with Attention (ADPA) is a novel approach in multi-agent reinforcement learning (MARL) that addresses challenges in large-scale, dynamic multi-agent environments. This repository contains the implementation of ADPA, which integrates an attention mechanism into decentralized policy learning to enhance agent performance and adaptability.

## Features
- **Decentralized Policy Learning**: Enables individual agents to learn effective strategies in a multi-agent environment.
- **Attention Mechanism**: Dynamically focuses on relevant information, improving decision-making in complex scenarios.
- **Scalable Architecture**: Efficiently handles an increasing number of agents without significant degradation in performance.
- **Versatile Application**: Suitable for cooperative, competitive, and mixed multi-agent environments.

## Environments
ADPA has been evaluated in various simulated environments, including:
- Cooperative Treasure Collection
- Rover-Tower Task

## Requirements
* Python 3.6.1 (Minimum)
* [OpenAI baselines](https://github.com/openai/baselines), commit hash: 98257ef8c9bd23a24a330731ae54ed086d9ce4a7
* [PyTorch](http://pytorch.org/), version: 0.3.0
* [OpenAI Gym](https://github.com/openai/gym), version: 0.9.4
* [Tensorboard](https://github.com/tensorflow/tensorboard), version: 0.4.0rc3 and [Tensorboard-Pytorch](https://github.com/lanpa/tensorboard-pytorch), version: 1.0 (for logging)

## How to Run

All training code is contained within `main.py`. To view options simply run:

```shell
python main.py --help
```
The "Cooperative Treasure Collection" environment from our paper is referred to as `simple_world_comm_v3` in this repo, and `Rover-Tower` is referred to as `simple_speaker_listener_v4`.

## Usage

To run ADPA in a specific environment:
```python
from marllib import marl
from adpa import ADPA

# prepare env
env = marl.make_env(environment_name="mpe", map_name="simple_speaker_listener_v4"
agent = ADPA(env)

# Training
agent.train()

# Evaluation
agent.evaluate()
```
