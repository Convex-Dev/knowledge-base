alias:: Doubles

- ---
- Fractional number
	- 64-bit IEEE-754 representation
- [Learn more on Wikipedia](https://en.wikipedia.org/wiki/Double-precision_floating-point_format)
- ---
- Literal notation
	- Decimal part preceded by `.`
		- ``` clojure
		  42.0
		  42.84
		  ```
	- Scientific notation
		- ``` clojure
		  (= 1e3
		     1000.0)
		  ```
	- Positive infinity
		- ``` clojure
		  ##Inf
		  ```
	- Negative infinity
		- ``` clojure
		  ##-Inf
		  ```
	- [[Not a Number]]
		- ``` clojure
		  ##NaN
		  ```
- ---
- Useful [[convex.core]] functions
	- [[(ceil)]]
	- [[(double)]]
	- [[(double?)]]
	- [[(floor)]]
	- [[(nan?)]]