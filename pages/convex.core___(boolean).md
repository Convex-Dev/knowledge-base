alias:: (boolean)
type:: [[Function]]

- ---
- [[Casts]] any [[Value]] to a [[Boolean]]
	- [[Truthy]] values to [[Boolean/True]]
		- ``` clojure
		  (= (boolean 42)
		     true)
		  
		  (= (boolean "some text")
		     true)
		  
		  (= (boolean [:a :b])
		     true)
		  
		  (= (boolean true)
		     true)
		  ```
	- [[Falsy]] values to [[False]]
		- ``` clojure
		  (= (boolean nil)
		     false)
		  
		  (= (boolean false)
		     false)
		  ```