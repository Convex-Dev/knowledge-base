alias:: Strings

- ---
- String of [[Chars]] forming text
- Encoded as [[UTF-8]]
- ---
- Create [[Strings]]
	- Literal notation
		- Characters between `"` `"`
			- ``` clojure
			  "This is some text"
			  ```
		- Any `"` belonging to the [[String]] can be escaped `\ `
			- ``` clojure
			  "She said: \"Wow, Convex is amazing\""
			  ```
		- Likewise, special characters like new lines are escaped with `\`
			- ``` clojure
			  "First line\nSecond line"
			  ```
	- [[(str)]]
- ---
- [[Countable]] operations
	- [[(count?)]]
		- Returns the number of [[Bytes]] in the given [[String]]
		- ``` clojure
		  (= (count "Convex")
		     6)
		  
		  (= (count "Thé ou café ?")
		     15)
		  ```
	- [[(empty?)]]
		- Tests if a [[String]] is empty
		- ``` clojure
		  (= (empty? "")
		     true)
		  
		  (= (empty? "Some text")
		     false)
		  ```
	- [[(first)]]
		- Returns the first [[Char]]
		- ``` clojure
		  (= (first "Some text")
		     \S)
		  ```
	- [[(last)]]
		- Returns the [[Char]] from the last [[Byte]] in the [[String]]
			- ``` clojure
			  (= (last "Convex")
			     \x)
			  ```
		- Like [[(nth)]], returns [[Nil]] on incomplete characters
			- ``` clojure
			  (nil? (last "è_é"))
			  ```
	- [[(nth)]]
		- Returns the [[Char]] at the given [[Byte]] position (starting at 0)
			- ``` clojure
			  (= (nth "Some text"	
			          2)
			     \m)
			  ```
		- Returns [[Nil]] if the byte position does not point to a complete [[UTF-8]] character
			- ``` clojure
			  (nil? (nth "Thé ou café ?"
			             3))
			  ```
	- [[(second)]]
		- Returns the [[Char]] from the second [[Byte]] in the [[String]]
			- ``` clojure()
			  (= (second "Convex")
			     \0)
			  ```
		- Like [[(nth)]], returns [[Nil]] on incomplete characters
			- ``` clojure
			  (nil? (second "è_é"))
			  ```