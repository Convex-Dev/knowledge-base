alias:: (char)

- ---
- [[Casts]] a [[Value]] to a [[Char]] when possible
- Discards high bits of larger [[Integers]]
- ---
- Supported types
	- [[Byte]]
		-
	- [[Double]]
		- ``` clojure
		  (= (char 97.0)
		     \a)
		  ```
	- [[Long]]
		- ``` clojure
		  (= (char 97)
		     \a)
		  ```
- All other types result in a [[Cast error]]