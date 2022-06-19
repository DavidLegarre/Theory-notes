# Thompson Sampling
As an alternative to [[Epsilon-greedy]], in order to improve how the algorithm explores.
We assume the reward of each action follows a Gaussian distribution.

For each action, we estimate its mean, and adjust the variance proportionally to the number of times we played that action in the past.
* The more an action is explored, the lower its variance, and viceversa.
* This variance captures our confidence that the estimation of the reward is correct.

![[Pasted image 20220619204431.png]]

Observe how the mean is stored in the Q-table (since it is the value we are expecting to obtain as a reward), and the [[Standard deviation]] will be defined as $\frac{1}{\text{number of times action taken}}$. 