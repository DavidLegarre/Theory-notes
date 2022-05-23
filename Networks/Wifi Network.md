# Wifi Network
We have an Access Point (AP) that transmits data packets to our Station (STA). In order to avoid collisions, the AP chooses at random a delay from a contention window (CW), in the range $[0,CW]$, to wait before starting transmission. This way chances of two STAs starting to transmit at the same time become smaller. 

Then, the receiver of this packet sends and ACK (acknowledge) packet, signaling that it has received it correctly. The time the system waits for this ACK is called SIFS (Short InterFace Space), this is necessary for the AP to switch the antenna from transmit mode to receive mode. 

![[Pasted image 20220523225633.png]]

Since in this cases, the wifi is a half-duplex connection, we cannot send and receive at the same time. After some amount of time DIFS (Distributed InterFace Space), this process will begin again, this is done so that we can make sure that the channel is empty before starting another transmission.

![[Pasted image 20220523225735.png]]

## Multiple nodes connection
When more than one STA is connected to the same AP the channel is shared using the protocol CSMA/CA.

![[Pasted image 20220523230132.png]]

This is done by random access, each node decides when to transmit.

In CSMA/CA before transmitting to a channel the nodes have to be listening the channel for a period of time and have to observe that the channel is not in use. In case of collision, both parts take another random number from the CW and try again. To avoid collisions we increase the range of random numbers to pick from, at the cost of an increase in delay since now we can take a larger number of ticks to wait than before.

## Binary exponential Backoff (BO)
When we transmit the BO for the first time it takes a value between $[0, CW_{min}]$

![[Pasted image 20220523230538.png]]

We keep increasing this R value to avoid collisions up to a max value ($CW_{max}$)

