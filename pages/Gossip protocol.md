alias:: Gossip

- ---
- [[Peer-to-peer]] communication through rounds of "gossiping"
- Initially, a node sends a message to a subset of other nodes in the network
- During the next round, those nodes propagate  the message likewise
	- To their chosen subsets of other nodes
- Merely a few rounds will suffice to propagate this message everywhere
	- Even in a substantial network
	- Due to the exponential effects of this behavior