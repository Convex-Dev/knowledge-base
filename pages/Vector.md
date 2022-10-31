alias:: Vectors
---

- [[Random-access]] [[Sequential]] [[Collection]] where values are referred to by their position
- ---
- Create a new [[Vector]] from scratch
	- Literal notation
		- Any number of [[Values]] in between `[ ]`
		- Commonly separated by space
			- `,` is also legal but not widely used unless it improves readability
		- ``` clojure
		  []
		  
		  [1 2 3]
		  [1, 2, 3]
		  
		  [:Convex ["is" "Awesome"]]
		  ```
	- [[(vector)]]
- ---
- Retrieve a [[Value]] by position
	- Using [[Vectors]] as [[Functions]]
		- ``` clojure
		  (= ([:a :b :c] 0)
		     :a)
		  
		  (= ([:a :b :c] 2)
		     :c)
		  ```
	- [[(get)]]
		- ``` clojure
		  (= (get [:a :b :c]
		          2)
		     :c)
		  
		  (nil? (get [:a :b :c]
		             3))
		  
		  (= (get [:a :b :c]
		          3
		          :x)
		     :x)
		  ```
	- [[(get-in)]]
		- ``` clojure
		  (= (get-in [:a [:b :c]]
		             [1 0])
		     :b)
		  
		  (nil? (get-in [:a [:b :c]]
		                [1000 42]))
		  
		  (= (get-in [:a [:b :c]]
		             [1000 42]
		             :not-found)
		     :not-found)
		  ```
- ---
- Create new [[Vectors]] by appending [[Values]] or other [[Collections]]
	- [[concat]]
		- ``` clojure
		  (= (concat [:a :b]
		             [:c :d])
		     [:a :b :c :d])
		  ```
	- [[(conj)]]
		- ``` clojure
		  (= (conj [:a :b]
		           :c)
		     [:a :b :c])
		  ```
	- [[(into)]]
		- ``` clojure
		  (= (into [:a :b]
		           (list :c :d))
		     [:a :b :c :d])   
		  ```
- ---
- Create new [[Vectors]] by removing values
	- [[(empty)]]
		- ``` clojure
		  (= (empty [:a :b :c])
		     [])
		  ```
	- [[(filter)]]
		- ``` clojure
		  (= (filter (fn [x]
		               (>= x 0))
		             [1 -42 0 42 -100])
		     [1 0 42])
		  ```
	- [[(next)]]
		- ``` clojure
		  (= (next [:a :b :c])
		     [:b :c])
		  ```
- ---
- Create new [[Vectors]] by replacing values
	- [[(assoc)]]
		- ``` clojure
		  (= (assoc [:a :b :c]
		            1
		            :X)
		     [:a :X :c])
		  ```
	- [[(assoc-in)]]
		- ``` clojure
		  (= (assoc-in [:a [:b :c]]
		               [1 0]
		               :X)
		     [:a [:X :c]])
		  ```
	- [[(map)]]
		- ``` clojure
		  (= (map (fn [x]
		            (+ x 42))
		          [1 2 3])
		     [43 44 45])
		  ```
- ---
- Create new [[Vectors]] by transformation
	- [[(reverse)]]
		- ``` clojure
		  (= (reverse [:a :b :c])
		     [:c :b :a])
		  ```
	- [[(vec)]]
- ---
- [[Predicates]]
	- [[(coll?)]]
		- ``` clojure
		  (= (coll? [:a :b :c])
		     true)
		  ```
	- [[(contains-key?)]]
		- ``` clojure
		  (= (contains-key? [:a :b :c]
		                    1)
		     true)
		  
		  (= (contains-key? [:a :b :c]
		                    42)
		     false)
		  ```
	- [[(vector?)]]
- ---
- [[Countable]] operations
	- [[(count)]]
		- ``` clojure
		  (= (count [:a :b :c])
		     3)
		  ```
	- [[(empty?)]]
		- ``` clojure
		  (= (empty? [])
		     true)
		  
		  (= (empty? [:a :b :c])
		     false)
		  ```
	- [[(first)]]
		- ``` clojure
		  (= (first [:a :b :c])
		     :a)
		  ```
	- [[(last)]]
		- ``` clojure
		  (= (last [:a :b :c])
		     :c)
		  ```
	- [[(nth)]]
		- ``` clojure
		  (= (nth [:a :b :c]
		          2)
		     :c)
		  ```
	- [[(second)]]
		- ``` clojure
		  (= (second [:a :b :c])
		     :b)
		  ```
-