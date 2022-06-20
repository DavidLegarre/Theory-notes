# Link Layer
<<<<<<< Updated upstream
In a typical connection we have multiple nodes connected in a half-duplex manner (the connection allows communication in both directions but only one direction at a time). 
=======
In a typical [[Wi-Fi Network]] we have multiple nodes connected in a half-duplex manner (the connection allows communication in both directions but only one direction at a time). 
>>>>>>> Stashed changes
The channel access arbitration is done using the **Distributed Coordination Function (DCF)** 

## Binary Exponential Backoff
![[Pasted image 20220425230322.png]]


## Automatic ReQuest Protocol (Stop & Wait)
* Unconfirmed packets are retransmitted until they are acknowledged or discarded
* There is a maximum number of retransmissions: $R_{max}$
* Stop & Wait ARQ protocol, where we send and ACK package where we specify everything has gone fine
![[Pasted image 20220425230545.png]]

* **SIFS**: Short InterFrame Space, the amount in microseconds required for a wireless interface to process a received frame and to response with a response frame.
* **DIFS**: DCF InterFrame Space, is a space used by the DCF to know if it's safe to send packets if nothing happens during this period.

![[Pasted image 20220425230728.png]]![[Pasted image 20220425230734.png]]

# CSMA / CA
* **Carrier Sense Multiple Acces(CSMA)**:  a protocol in which a node verifies the absence of other traffic before transmitting on a shared transmission medium.
 