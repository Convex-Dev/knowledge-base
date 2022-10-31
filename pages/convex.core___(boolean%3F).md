alias:: (boolean?)
type:: [[Function]]

- ---
- [[Predicate]] returning
	- [[Boolean/True]] if the argument is a [[Boolean]]
		- ``` clojure
		  (= (boolean? true)
		     true)
		  
		  (= (boolean? false)
		     false)
		  ```
	- [[False]] for any other [[Type]]
		- ``` clojure
		  (= (boolean? 42)
		     false)
		  
		  (= (boolean? nil)
		     false)
		  ```