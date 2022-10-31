- Property of a programming language
- Programs expressed in that language can be manipulated as [[Data]] via this language
- Leading to very efficient [[Metaprogramming]]
- ---
- Example
	- Suppose this [[Function]]
		- ``` clojure
		  (fn [x]
		    (* x x))
		  ```
	- It is expressed in terms of
		- [[List]]
		- [[Symbol]]
		- [[Vector]]
	- This, [[Convex Lisp]] is homoiconic
		- Expressed in terms of [[Values]]
		- Explicitly designed for manipulating those [[Values]] efficiently