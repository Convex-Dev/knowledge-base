alias:: Consensus point

- ---
- Number of [[Confirmed blocks]]
- Represents the stable portion of the [[Ordering]]
	- Everything beyond this point are [[Unconfirmed blocks]]
- Each [[Peer]] maintains its own view of the consensus point
	- Based on observed [[Consensus proposals]] from other peers
	- In a way that is [[Eventually consistent]]