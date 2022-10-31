alias:: (str)
type:: [[Function]]

- ---
- Computes the [[String]] representations of the given [[Values]]
- ---
- No argument returns an empty [[String]]
	- ``` clojure
	  (= (str)
	     "")
	  ```
- 1 argument returns its printed form
	- ``` clojure
	  (= (str "Some text")
	     "Some text")
	  
	  (= (str 42)
	     "42")
	  
	  (= (str 42.84)
	     "42.84")
	  
	  (= (str [:a :b])
	     "[:a :b]")
	  
	  (= (str nil)
	     "nil"))
	  ```
- When more than 1 argument, representations are concatenated
	- ``` clojure
	  (= (str \C \o \n \v \e \x)
	     "Convex")
	  
	  (= (str "Some "
	          "text")
	     "Some text")
	  ```