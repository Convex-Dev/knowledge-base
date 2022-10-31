alias:: (quote), Quotation
type:: [[Special form]]

- ---
- Prevents [[Evaluation]]
- As a shortcut, prepending a [[Value]] with `'` has the same effect
- ---
- Examples
	- [[Symbol]] is merely returned instead of resolving to `42`
		- ``` clojure
		  (def x
		       42)
		  
		  (= x
		     42)
		  
		  (= (quote x)
		     (symbol "x"))
		  
		  (= 'x
		     (symbol "x"))
		  ```
	- What would otherwise evaluate to a [[Function]] is returned as a [[List]]
		- ``` clojure
		  (list? '(fn [x] (* x x)))
		  ```