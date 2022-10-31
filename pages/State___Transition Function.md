alias:: State Transition Function

- Function updating the [[State]]
- Applied by the [[Convex Virtual Machine]] when processing new [[Confirmed blocks]]
- Formally this might be recursively specified as:
	- #+BEGIN_QUOTE
	  S[n+1] = f(S[n], B[n])
	  
	  where:
	      f        is the State Transition Function
	      S[n]  is the sate after n blocks have been processed
	      B[n]  is the block at position n in the ordering
	      S[0]  is the pre-defined genesis state
	  #+END_QUOTE