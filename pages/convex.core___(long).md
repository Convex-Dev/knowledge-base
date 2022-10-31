alias:: (long)

- ---
- [[Casts]] a [[Value]] to a [[Long]]
- Supported [[Types]]
	- [[Blob]] (truncated beyond 64 bits)
		- ``` clojure
		  (= (long 0xffff)
		     65535)
		  ```
	- [[Boolean]]
		- ``` clojure
		  (= (long true)
		     1)
		  ```
	- [[Byte]]
		- ``` clojure
		  (= (long (byte 42))
		     42)
		  ```
	- [[Char]]
		- ``` clojure
		  (= (long \a)
		     97)
		  ```
	- [[Double]]
		- ``` clojure
		  (= (long 42.84)
		     42)
		  ```
	- [[Long]] ([[No-op]])
		- ``` clojure
		  (= (long 42)
		     42)
		  ```