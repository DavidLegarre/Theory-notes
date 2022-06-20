# Q-Table
Q-Table is a table that is formed to use in [[Reinforcement learning]] to store the action-value estimates. Given a set of states and a set of actions:

We define the Q-table as a matrix of shapes: $(states\times actions)$. In each cell of this matrix, we will store the reward learned: $Q_{ij}$ stores the reward if we take action $j$ when the system is at state $i$. 

![[Pasted image 20220620174233.png]]
Actions Remain and Switch in the channel selection problem