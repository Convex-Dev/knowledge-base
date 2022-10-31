- Numerical value used to refer to an [[Account]]
	- Internally represented as a specialized 8-byte [[Blob]]
	- Hence, can act as keys in [[Blob-Map]]
- The [[Convex Virtual Machine]] issues new addresses sequentially when creating [[Accounts]]
- ---
- Create an [[Address]]
	- Literal notation
		- Natural number prefixed with `#`
		- ``` clojure
		  #1
		  #42
		  #1234567890
		  ```
	- [[(address)]]
- ---
- Important [[convex.core]] [[Values]]
	- [[*address*]]
	- [[*caller*]]
- ---
- [[Predicate]]
	- [[(address?)]]
- ---
- Transfers to other [[Accounts]]
	- [[Convex Coins]]
		- ``` clojure
		  (transfer #42
		            1000)
		  ```
	- [[Memory]]
		- ``` clojure
		  (transfer-memory #42
		                   1000)
		  ```
- ---
- Convert to other [[Types]]
	- [[(blob)]]
		- ``` clojure
		  (= (blob #42)
		     0x000000000000002a)
		  ```
	- [[(long)]]
		- ``` clojure
		  (= (long #42)
		     42)
		  ```