# Throughput of data
## Definition
In communication networks, *network throughput* is defined as the rate of successful message delivery over a communication channel in a time period.
$$Throughput=\frac{\text{amount of data}}{\text{time}}$$
$$Pr(\text{Transmission})(\tau)=\frac{\# \text{of slots with }Tx}{\text{Total Number of slots}}$$
## Example of connection
![[Pasted image 20220427174420.png]]

In order to prevent collision we add random Backoff (random waiting time), we then define $CW_{min}$ as the Contention Window (as the number of different Backoff)
![[Pasted image 20220427175716.png]]

![[Pasted image 20220426004424.png]]

Average Backoff values: $E[B]$, we then have that $$\tau=\frac{1}{E[B]+1}$$

