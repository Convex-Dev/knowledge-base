alias:: (not)
type:: Function

- ---
- Opposite of [[(boolean)]]
- Converts
	- [[Truthy]] values to [[False]]
		- ``` clojure
		  (= (not true)
		     false)
		  
		  (= (not 42)
		     false)
		  
		  (= (not "some text")
		     false)
		  
		  (= (not [:a :b])
		     false)
		  ```
	- [[Falsy]] values to [[Boolean/True]]
		- ``` clojure
		  (= (not false)
		     true)
		     
		  (= (not nil)
		     true)
		  ```