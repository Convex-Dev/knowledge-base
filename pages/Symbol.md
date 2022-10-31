alias:: Symbols

- ---
- [[Value]] acting as a name
- Evaluates to a [[Lookup]] unless prevented
- ---
- Literal notation
	- Up to 128 bytes of [[UTF-8]] characters without anything else around it
		- ``` clojure
		  some-symbol
		  another-symbol
		  ```
- ---
- Create a symbol
	- [[(quote)]]
		- Since quoting prevents [[Evaluation]], the [[Symbol]] remains as it is and no [[Lookup]] is performed
		- ``` clojure
		  'some-symbol
		  ```
	- [[(symbol)]]
		- ``` clojure
		  (= 'some-symbol
		     (symbol "some-symbol"))
		  ```
- ---
- Other useful [[Functions]]
	- [[(str)]]
		- ``` clojure
		  (= (str 'some-symbol)
		     "some-symbol")
		  ```