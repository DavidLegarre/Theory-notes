# Upper Confidence Bound UCB

The upper confidence bound (UCB) action-selection strategy is based on the principle of optimism in the face of uncertainty.

- In each round, UCB selects the arm expected to give us the highest reward.
- Intuitively, UCB trades off exploration and exploitation:
	- Upon every time a suboptimal arm is chosen, the corresponding confidence bound will shrink significantly
	- Thus, quickly decreasing the probability of drawing this arm in the future.

According to equation:
$$
\sqrt{\frac{2\log(t)}{\text{Times action }a\text{ taken}}}
$$
