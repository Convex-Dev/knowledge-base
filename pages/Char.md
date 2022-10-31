alias:: Chars

- ---
- Characters: letters, digits, punctuation, ...
- [Learn more on Wikipedia](https://en.wikipedia.org/wiki/Character_(computing))
  id:: 63650e9a-981f-4c50-ae2c-12416b357e38
- ---
- Literal notation
	- Printable chars are prefixed with `\`
		- ``` clojure
		  \C \o \n \v \e \x
		  \?
		  \!
		  ```
	- Supported non-printable characters
		- ``` clojure
		  \newline
		  \return
		  \space
		  \tab
		  ```
	- [[Unicode]]
		- ``` clojure
		  (= \u0061
		     \a)
		  ```
- ---
- Related [[convex.core]] functions
	- [[(char)]] ([[No-op]])
		- ``` clojure
		  (= (char \a)
		     \a)
		  ```
	- [[(long)]]