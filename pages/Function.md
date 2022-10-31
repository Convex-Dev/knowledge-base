alias:: Functions

- ---
- [[Value]] containing [[Code]] to execute given some [[Arguments]]
- Like any other value, can be passed to and returned from other [[Functions]]
- ---
- Notation
	- ``` clojure
	  (fn [...<args>] 
	    ...<body>)
	  ```
- ---
- Examples
	- No argument, does not do anything
		- ``` clojure
		  (fn [])
		  ```
	- Returns `x` squared
		- ``` clojure
		  (fn [x]
		    (* x x))
		  ```
	- [[Variadic]] inputs, computes the sum of the given numbers
		- ``` clojure
		  (fn [& numbers]
		    (reduce +
		            0
		            numbers))
		  ```
- ---
- See
	- [[(defn)]] as a shortcut for defining [[Functions]]
	- [[Closures]]
	- [[Multi-functions]]