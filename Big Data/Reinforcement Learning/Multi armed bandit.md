# Multi-armed bandit (MAB)
The Multi-armed Bandit problem is used in [[Reinforcement learning]] to formalize the notion of decision-making under uncertainty. In a multi-armed bandit problem, an agent chooses between $k$ different actions and receives reward base on the chosen action. 

## Action-value & Action-value estimate
For an agent to decide which action yields the maximum  reward, we must define the value of making each action. We use the concept of probability to define these values using the action-value function.
The value of selecting an action is defined as the expected reward received when taking that action from a set of possible actions. Since the value of selecting an action is unkown to the agent, we use the 'sample-average' method to estimate the value of taking an action.

![[Pasted image 20220618200426.png]]


# Exploration vs Exploitation
* **Exploration** is a phase where we allow an agent to improve their knowledge about each action. Improving the accuracy of the estimated action-values, enabling the agent to make more informed decisions in the future.

* **Exploitation** is the phase where the agent chooses the greedy action to get the most reward by exploiting the agent's current action-value estimates.

When agent explores it gets more **accurate** estimations of action-values. And when it exploits, it might get more **reward**. It **cannot do both**.
![[Pasted image 20220619200118.png]]

# Types of algorithms
We have:
* [[Epsilon-greedy]]
* 