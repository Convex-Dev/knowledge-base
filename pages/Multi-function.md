alias:: Multi-functions

- ---
- [[Function]] specifying several implementations varying by [[Arity]]
- Each [[Arity]] with its body is enclosed between `( )`
- ---
- Often used for making [[Arguments]] optional
	- ``` clojure
	  (defn say-hi
	    
	    ([]
	     (say-hi "John Doe"))
	    
	    ([name]
	     (str "Hi " name "!")))
	  
	  
	  (= (say-hi)
	     "Hi John Doe!")
	  
	  (= (say-hi "Alice")
	     "Hi Alice!")
	  ```