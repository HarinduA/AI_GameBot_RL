# 🎮 AI Game Bot – CartPole with Q-Learning

An AI bot that learns to play the classic **CartPole-v1** game using **Reinforcement Learning (Q-Learning)**. Built with Python and OpenAI Gym, the agent learns to balance a pole by maximizing rewards through exploration and exploitation.

---

## 🧠 What It Does

- Trains an agent to play CartPole using Q-learning (discretized state space)
- Visualizes learning progress with reward plots
- Optionally renders live gameplay after training

---

## 📁 Project Structure

AI_GameBot_RL/
│
├── train_bot.py              # Main script: trains the Q-learning agent on CartPole
├── requirements.txt          # Python dependencies (optional but recommended)
├── README.md                 # Project overview, setup, usage instructions
│
├── results/                  # Output folder for training plots
│   └── rewards_plot.png      # Saved graph of total rewards per episode
│
└── venv/                     # Virtual environment (not included in Git, add to .gitignore)


## ✅ Requirements

Make sure you're using **Python 3.11**.

Install dependencies:

```bash
pip install pygame==2.6.1
pip install gym==0.26.2 --no-deps
pip install "gym[classic_control]" --no-deps
pip install numpy==1.24.4 matplotlib
pip install cloudpickle gym-notices
▶️ How to Run
🏋️‍♂️ Train the Agent:
bash
Copy
Edit
python train_bot.py
This will:

Train the agent for 1000 episodes

Print performance logs

Save a reward plot to results/rewards_plot.png

👀 Watch the Bot Play:
In train_bot.py, enable rendering by uncommenting this line:

python
Copy
Edit
if ep > 800:
    env.render()
This will open a game window during the final episodes so you can watch your agent balance the pole!

📊 Example Output
yaml
Copy
Edit
Episode 100: Reward = 23.0, Epsilon = 0.90
Episode 500: Reward = 120.0, Epsilon = 0.12
Episode 1000: Reward = 210.0, Epsilon = 0.01
Reward graph is saved automatically to:

bash
Copy
Edit
results/rewards_plot.png
💡 Notes
np.bool8 was removed in NumPy 2.2+, so we use numpy==1.24.4 to maintain compatibility with gym==0.26.2.

--no-deps is used to avoid Gym trying to install incompatible pygame==2.1.0.

🚀 Future Ideas
🧠 Deep Q-Learning (DQN) with a neural network

💾 Model saving/loading for replay

🧪 Evaluation script without training

