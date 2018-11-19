# Reinforcement Learning: Deeq Q Learning Network (DQN) Agent playing Atari Breakout
* Training a vision-based agent with the Deep Q Learning Network (DQN) in Atari's Breakout environment, implementation in Tensorflow.

## Environment
* **< Python 3.7 >**
* **< [OpenAI Gym](https://github.com/openai/gym) >**
	- Type the following commands to install OpenAI Gym Atari environment:
	`$ pip3 install opencv-python gym "gym[atari]"`
	- Atari environment used: `BreakoutNoFrameskip-v4`
* **< [Tensorflow r.1.12.0](https://www.tensorflow.org/) >**

## Implementation
* Deep Q Learning Network with the following improvements:
	- Experience Replay
	- Fixed Target Q-Network
	- TD error loss function with: *Q<sub>target</sub> = reward + (1-terminal) * (gamma * Q<sub>max</sub>(s’) )*
* DQN network Settings:
![]()

## File Description
```
.
├── ./
|   ├── agent_dir.py                			DQN model
|   ├── atari_wrapper.py                   		Atari wrapper
|   ├── environment.py                			Gym wrapper
|   ├── runner.py            					Main program for training and testing
|   ├── Readme.md    							This file
└── model/
	├── dqn_learning_curve_compare.png         
	├── dqn_best_setting.png     
	├── dqn_learning_curve.png       
	├── checkpoint
	├── model_dqn-25581.data-00000-of-00001
	├── model_dqn-25581.meta
	└── model_dqn-25581.index
```

## Usage
* Traing the DQN Agent: `$ python3 runner.py --train_dqn`
* Testing the DQN Agent: `$ python3 runner.py --test_dqn`
* Testing the DQN Agent with **gameplay rendering**: `$ python3 runner.py --test_dqn --do_render`

## Learning Curve
* Single learning curve:
![]()
* With different plotting window: