- Convex uses Stakes to determine the voting weight of each Peer in the Consensus Algorithm.
  
  Benefits for a Peer having a higher effective voting stake are:
- Slightly more influence over which Blocks get ordered first, if two blocks are simultaneously submitted for consensus
- They may also benefit from slightly improved overall latency for Blocks that they submit.
  
  While good Peers are expected to be content neutral, they may legitimately wish to offer better QoS to their partners or customers, and having a higher voting stake can help them to achieve this.
  
  The protocol does not allow Peers to reverse a confirmed consensus, or prevent (censor) a Block from being included in consensus. Their stake may be at risk if they attempt this.