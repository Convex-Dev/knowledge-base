alias:: Blob, Blobs

- ---
- Arbitrary sequence of [[Bytes]]
- ---
- Create a new [[Blob]]
	- Literal notation
		- [[Hex string]] prepended with `0x`
			- `0x` alone is an empty [[Blob]]
		- ``` clojure
		  0x01
		  0x42
		  0xff23789875
		  ```
	- [[(blob)]]
- ---
- [[Predicate]]
	- [[(blob?)]]
- ---
- [[Countable]] operations
	- [[(count)]]
		- ``` clojure
		  (= (count 0x0102ff)
		     3)
		  ```
	- [[(first)]]
		- ``` clojure
		  (= (first 0x0102ff)
		     1)
		  ```
	- [[(nth)]]
		- ``` clojure
		  (= (nth 0x0102ff
		          2)
		     255)
		  ```
	- [[(second)]]
		- ``` clojure
		  (= (second 0x0102ff)
		     2)
		  ```