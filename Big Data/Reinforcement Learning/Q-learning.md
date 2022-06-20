# Q-Learning
Is an algorithm that by using a [[Q-Table]] and an algorithm to explore the state space from [[Multi armed bandit]] using the following equation to update the Q-table:

$$
Q_{old}(s_{t},a_{t})
+\alpha\cdot(r_{t}+\gamma\cdot\underset{a}{\max}Q(s_{t+1},a)
-Q_{old}(s_{t},a_{t}))
$$

Where, $\alpha$ is the learning rate, $r_{t}$ is the reward, $\gamma$ is the discount factor.

* With $\alpha\in[0,1]$, being $0$ we don't learn, and $1$ we use only instantaneous information.
* With  $\gamma\in[0,1]$ determines the importance of future rewards
	*  $0$: only rewards from current state are considered
	* $1$: only considers "expectations", may create instability (better to set lower values)

![[Pasted image 20220620175036.png]]

![[Pasted image 20220620175042.png]]

![[Pasted image 20220620175050.png]]


