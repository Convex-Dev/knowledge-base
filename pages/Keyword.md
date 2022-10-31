alias:: Keywords

- ---
- [[Value]] acting as a name
- However, unlike [[Symbol]], does not evaluate to anything else
- ---
- Create a [[Keyword]]
	- Literal notation
		- `:` followed by at most 128 bytes of [[UTF-8]] characters
		- ``` clojure
		  :some-keyword
		  :another-keyword
		  ```
	- [[(keyword)]]
- ---
- [[Predicate]]
	- [[(keyword?)]]
- ---
- [[Casting]]
	- [[(str)]]
		- ``` clojure
		  (= (str :some-keyword)
		     "some-keyword")
		  ```
	- [[(symbol)]]
		- ``` clojure
		  (= (symbol :some-keyword)
		     'some-symbol)
		  ```