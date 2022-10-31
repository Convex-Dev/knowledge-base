alias:: Bytes

- ---
- 8-bit unsigned [[Integer]]
- Range (inclusive)
	- Minimum
		- `0`
	- Maximum
		- `255`
- ---
- Create a [[Byte]]
	- Unlike most [[Types]], no literal notation
	- [[(byte)]]
- ---
- Convert to other [[Types]]
	- [[(char)]]
		- ``` clojure
		  (= (char (byte 97))
		     \a)
		  ```
	- [[(double)]]
		- ``` clojure
		  (= (double (byte 97))
		     97.0)
		  ```
	- [[(long)]]
		- ``` clojure
		  (= (long (byte 97))
		     97)
		  ```
	- [[(str)]]
		- ``` clojure
		  (= (str (byte 97))
		     "97")
		  ```
- ---
- Also see [[Integer]] for more operations
	- [[Bytes]] are always promoted to [[Longs]]