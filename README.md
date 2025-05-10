# Snake AI using Deep Q-Learning

This project implements an AI agent that learns to play the classic Snake game using Deep Q-Learning (DQN). The agent learns to maximize its score by eating food while avoiding collisions with walls and itself.

## Features

- Deep Q-Learning implementation
- Real-time visualization of training progress
- Automatic model saving for best performance
- Configurable game parameters
- Pygame-based game environment

## Requirements

```bash
torch>=2.0.0
numpy>=1.21.0
pygame>=2.1.0
matplotlib>=3.4.0
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/lakshaybishnoi/snake_ai_dqn.git
cd snake_ai_dqn
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

To start training the AI:
```bash
python train.py
```

The training process will:
- Show the Snake game window
- Display a real-time plot of training progress
- Save the best model automatically
- Print current score and record score

## Project Structure

- `game.py`: Snake game environment implementation
- `model.py`: Neural network and training logic
- `agent.py`: AI agent implementation
- `train.py`: Main training loop
- `helper.py`: Visualization utilities

## How it Works

The AI uses a Deep Q-Network with:
- 11 input features (game state)
- 256 hidden neurons
- 3 output actions (straight, right turn, left turn)

The agent learns through:
- Experience replay
- Epsilon-greedy exploration
- Reward-based learning
  - +10 for eating food
  - -10 for collisions
  - +1 for moving closer to food
  - -0.1 for not making progress

## Training Progress

The training progress is visualized in real-time showing:
- Current score
- Mean score
- Number of games played

## License

This project is open source and available under the MIT License.

## Author

Lakshay Bishnoi 