# Throughput of data
Specifically calculated from a [[Wi-Fi Network]].

## Definition
In communication networks, *network throughput* is defined as the rate of successful message delivery over a communication channel in a time period.
$$Throughput=\frac{\text{amount of data}}{\text{time}}$$
![[Pasted image 20220523230706.png]]


## Transmission probability
![[Pasted image 20220523231042.png]]

Where Tx means transmissions. 

But we can see that that is not a representative sample. Since after a period of time we'd see that the $\tau$ would ressemble mor of a function like

$$
\tau=\frac{1}{E[B]+1}
$$

Where $E[B]$ is the average backoff values, that with the $CW$ of the previous case ($15$) would be:

$$
E[B]=\frac{CW_{min}}{2}=\frac{15}{2}=7.5
$$
Then:

$$
\frac{2}{13}\not=\frac{1}{7.5+1}
$$
Hence, $\frac{2}{13}$ is not a representative transmission probability of the connection.

In order to ==increase the throughput, we must transmit more data in less time== 

## Collision probability 
We then define the collision probability as:

$$
p=1-(1-\tau)^{N-1}
$$
With $N$ as the number of STAs.
In a network we can assume that all devices Tx with the same $\tau$.

# Throughput
![[Pasted image 20220620195958.png]]

We can transmit 3 packets of size $L$ and each packet takes $Ts$ to process, then, we have 1 collision that it also takes $Ts$ to process since it still another packet to send, then we have 4 empty slots and each one takes $T_{e}s$  so with the formula of throughput in [[Throughput#Definition]]:
$$
Th=\frac{N_{s}\cdot L}{N_{e}\cdot T_{e}+(N_{s}+N_{c})\cdot T}
$$

Where $N_{s}:$ Number of successes, $N_{e}:$ number of empty slots, $N_{c}:$  number of collisions

# Throughpout as probabilities

![[Pasted image 20220523232233.png]]

Then:
* $p_{e}=(1-\tau)^{N}$ 
* $p_{s}=N\tau(1-\tau)^{N-1}$ 
* $p_c=1-p_{e}-p_{s}$ 

![[Pasted image 20220620200738.png]]


