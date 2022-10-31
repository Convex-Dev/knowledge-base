alias:: Blocks

- ---
- Collection of [[Transactions]] submitted simultaneously by a [[Peer]]
- Contains a [[Timestamp]] issued by that Peer
- ---
- On a conventional [[Blockchain]]
	- Blocks are linked cryptographically
		- Each block contains the [[Hash]] of the previous block
	- Produced sequentially
		- Typically, a leader gains the right to emit a block
- On [[Convex]]
	- Blocks are ordered using [[Convergent Proof of Stake]]
		- No need to link them cryptographically
	- Produced concurrently
		- Any [[Peer]] can broadcast a new block at any moment
	- Broadcasted using [[Gossip]]