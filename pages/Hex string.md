- [[String]] representing [[Bytes]]
- Each byte is encoded in [[Hexadecimal]]
	- Hence the number of characters is always even
- ---
- Examples
	- 1 byte
		- ``` clojure
		  "01"
		  "42"
		  "ff"
		  ```
	- 3 bytes
		- ``` clojure
		  "42ff1a"
		  "01bc78"
		  "35aadc"
		  ```