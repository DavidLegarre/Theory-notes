# Markov Decision Process
We can use a Markov  Decision Process (MDP) if, the next state of the process depends only on the current state.

In MDP we have:
* Set of states: **state of the space**
* Set of actions (these will depend on the current state)
* Transition probabilities (which depend on the actions we take)
* Rewards (which depends if our actions were good or bad)

Solving the MDP $\to$ **learning**: Finding the best action to take when we are in a given state

[[Q-learning]] is an algorithm to solve MDP