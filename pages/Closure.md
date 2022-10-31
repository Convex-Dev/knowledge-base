alias:: [[Closures]]

- ---
- Ability of a [[Function]] to capture and retain outer [[Bindings]] after they go out of [[Scope]]
- ---
- Example
	- [[Scope]] created by this [[(let)]] becomes inaccessible being executed
	- ``` clojure
	  (let [x 42]
	    (defn my-function
	      [y]
	      (+ x y)))
	  ```
	- However, the [[Function]] initially defined inside of it still has access to it
	- ``` clojure
	  (= (my-function 1)
	     43)
	  ```