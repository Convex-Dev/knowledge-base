- [[Value]] representing the absence of a [[Value]]
- Sometimes
	- Data is missing or might not be available yet
	- A result cannot be produced
	- A computation does not return an output
	- ...
- [[Nil]] is then used as a placeholder
- ---
- Many programming languages have a concept of [null](https://en.wikipedia.org/wiki/Null_pointer) references
	- However, `null` often leads to puzzling bugs
	- In Convex, [[Nil]] is a first-class citizen, a [[Value]] like any other
- ---
- Literal notation
	- ``` clojure
	  nil
	  ```
- ---
- [[Predicate]]
	- [[(nil?)]]
		- ``` clojure
		  (= (nil? nil)
		     true)
		  
		  (= (nil? 42)
		     false)
		  ```