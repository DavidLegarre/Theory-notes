# $\epsilon$-greedy algorithms
We will define our [[Q-Table]] of size $K$ (one position for each action), all set to 0.
Once we have our [[Q-Table]] built, we may decide for the pure greedy function where we only choose the maximum reward. 
In $\epsilon$-greedy algorithms, we define that with $p=\epsilon$ the system will try a random option and add this reward to our Q-table, and then maximize this new Q-table.
* At $t=0$:
	* The agent selects an action from $\mathit{A}$ uniformly at random: $P(\mathit{A}(t)=a)=\frac{1}{k}$ 
	* We obtain the corresponding reward
	* We increase the number of attempts we take action $a:n_{a}=n_{a}+1=1$
	* We update the $Q$-table: $Q(A(0))=\frac{Q(A(0)(n_{a}-1))V(0)}{n_{a}}$
	* We increase the accumulated reward $W$
	
* At $t>0$ , repeat, until $t=T$
	* At time $t$ the agent decides:
		* To explore with probability: $\epsilon$, Next action is selected uniformly randomly from $A$ 
		* To exploit with probability: $1-\epsilon$, next action is $A(t)=argmax_{a\in A}Q(a)$ 
	* We obtain the corresponding reward 
	* We increase the number of attempts we take action $a$
	* We update the $Q$-table
	* We increase the accumulated reward $W$ 

![[Pasted image 20220619195025.png]]

## Updating Q-Table
To update the Q-table we use equation

$$
Q_{new}(a)=\frac{Q_{old}(a)\cdot(n_{a}-1)+(1-\rho)}{n_{a}}
$$
Where $\rho$ is the reward of the action, and $n_a$ is the number of times action $a$ is selected