# My Reinforcement Learning Implementation

## Overview

In this project, I will implement Value Iteration and Q-Learning algorithms to solve Markov Decision Processes (MDPs). I'll be testing my agents on Gridworld, a simulated robot controller (Crawler), and Pacman environments.

## What I Need to Do

### Files I Need to Edit

1. `valueIterationAgents.py`

- I'll implement my Value Iteration agent here
- This will help me solve known MDPs

1. `qlearningAgents.py`

- I'll write my Q-Learning agents here
- I'll test them on Gridworld, Crawler, and Pacman

1. `analysis.py`

- I'll document my answers to project questions here

### Files I Should Read (But Not Edit)

- `mdp.py`: Contains methods for general MDPs
- `learningAgents.py`: Has the base classes I'll extend
- `util.py`: Includes utilities (especially `util.Counter` for my Q-learner)
- `gridworld.py`: The Gridworld implementation
- `featureExtractors.py`: Features for Approximate Q-Learning

## How I'll Get Started

### Running Gridworld

I can start by running Gridworld in manual mode:

```
python gridworld.py -m
```

This will let me:

- Use arrow keys for control
- See how the agent moves (80% success rate)

To see all my options:

```
python gridworld.py -h
```

## What I Need to Implement

### Value Iteration (Q1)

In `valueIterationAgents.py`, I need to implement:

1. `computeActionFromValues(state)`
1. `computeQValueFromValues(state, action)`

To test my implementation:

```
python autograder.py -q q1
```

To visualize my agent:

```
python gridworld.py -a value -i 100 -k 10
```

### Q-Learning (Q2)

In `qlearningAgents.py`, I need to implement:

1. `update(state, action, nextState, reward)`
1. `computeValueFromQValues(state)`
1. `getQValue(state, action)`
1. `computeActionFromQValues(state)`

Important notes for my implementation:

- Break ties randomly in `computeActionFromQValues`
- Only access Q-values through `getQValue`
- Remember unseen actions have Q-value of zero

To test my Q-learning agent:

```
python autograder.py -q q2
```

To run manual control:

```
python gridworld.py -a q -k 5 -m
```

## How I'll Test My Work

### Using the Autograder

I can test:

- python autograder.py
- python autograder.py -q q2
- python autograder.py -t test_cases/q2/1-bridge-grid

### Debugging Tips

If I run into issues, I can:

- Use `--noise 0.0` to turn off noise
- Use `-q` to quiet transition output
- Watch the console during graphical display

## Important Reminders

### Academic Integrity

I must:

- Submit my own work
- Not share or copy code
- Be aware that plagiarism detection will be used

### Getting Help

If I need help, I can:

- Go to office hours
- Use the discussion forum
- Contact course staff
- Review the Project 0 autograder tutorial

### Due Date

I must submit by December 8, 2024, at 11:59 PM Central

### Grading Notes

My grade will be based on:

- Autograder test results
- Possible manual code review
- Implementation correctness
- Using original function/class names

<br>
