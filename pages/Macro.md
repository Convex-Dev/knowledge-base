alias:: Macros

- ---
- Specialized [[Function]] used during [[Expansion]]
	- [[Arguments]] do not undergo [[Evaluation]] and are fed as they are
	- Output is [[Data]] aimed for [[Execution]]
- Allows extending the native capabilities of the [[Compiler]]
- Advanced feature
- ---
- Notation
	- ``` clojure
	  (defmacro <name>
	    [<...arguments>]
	    <body>)
	  ```
- ---
- Example
	- An `infix` macro converting [[Infix notation]] to the [[Prefix notation]] of [[Convex Lisp]]
	- Code to eventually execute is returned as [[Data]]
	- ``` clojure
	  (defmacro infix
	    [a f b]
	    (list f a b))
	  ```
	- When called, the returned [[Data]] goes through [[Compilation]] and [[Execution]]
	- ``` clojure
	  (= (infix 1 + 1)
	     (+ 1 1)
	     2)
	  ```
- ---
- A [[Macro]]
	- Cannot be defined and used in the same [[Transaction]]
	- Unlike a regular [[Function]], cannot be used as [[Argument]]