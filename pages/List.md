alias:: Lists

- ---
- [[Sequential]] [[Collection]]
- Commonly used for representing [[Function]] application
- ---
- Apply [[Arguments]] to a [[Function]]
	- To [[(+)]], apply `1` and `2`
	- ``` clojure
	  (+ 1 2)
	  ```
- ---
- Create a [[List]] without [[Evaluation]]
	- [[(list)]]
		- ``` clojure
		  (list :a :b :c)
		  ```
	- [[(quote)]]
		- ``` clojure
		  (= '(:a :b :c)
		     (list :a :b :c))
		  ```
- ---
- Retrieve a [[Value]] by position
	- Using [[Lists]] as [[Functions]]
		- ``` clojure
		  (= ('(:a :b :c) 1)
		     :b)
		  ```
	- [[(get)]]
		- Allows access beyond the capacity of the [[List]]
		- ``` clojure
		  (= (get '(:a :b :c)
		          1)
		     :b)
		  
		  (nil? (get '(:a :b :c)
		             42))
		  
		  (= (get '(:a :b :c)
		          42
		          :not-found)
		     :not-found)
		  ```
	- [[(get-in)]]
		- ``` clojure
		  (= (get-in '(:a [:b :c] :d)
		             [1 1])
		     :c)
		  
		  (nil? (get-in '(:a [:b :c] :d)
		                [42 1]))
		  
		  (= (get-in '(:a [:b :c] :d)
		             [42 1]
		             :not-found)
		     :not-found)
		  ```
- ---
- Create new [[Lists]] by adding [[Values]] or [[Collections]]
	- [[(concat)]]
		- ``` clojure
		  (= (concat '(:a :b)
		             [:c :d])
		     '(:a :b :c :d))
		  ```
	- [[(conj)]]
		- ``` clojure
		  (= (conj '(:a :b)
		           :c)
		     '(:c :a :b))
		  ```
	- [[(cons)]]
		- ``` clojure
		  (= (cons :c
		           '(:a :b))
		     '(:c :a :b))
		  ```
	- [[(into)]]
		- ``` clojure
		  (= (into '(:a :b)
		           [:c :d])
		     '(:d :c :a :b))
		  ```
- ---
- Create new [[Lists]] by removing values
	- [[(empty)]]
		- ``` clojure
		  (= (empty '(:a :b :c))
		     '())
		  ```
	- [[(filter)]]
		- ``` clojure
		  (= (filter (fn [x]
		               (>= x 0))
		             '(1 -42 0 42 -100)
		     '(1 0 42))
		  ```
	- [[(next)]]
		- ``` clojure
		  (= (next '(:a :b :c))
		     '(:b :c))
		  ```
- ---
- Create new [[List]] by replacing values
	- [[(assoc)]]
		- ``` clojure
		  (= (assoc '(:a :b :c)
		            1
		            :X)
		     '(:a :X :c))
		  ```
	- [[(assoc-in)]]
		- ``` clojure
		  (= (assoc-in '(:a (:b :c))
		               [1 0]
		               :X)
		     '(:a (:X :c)))
		  ```
- ---
- [[Predicates]]
	- [[(coll?)]]
		- ``` clojure
		  (= (coll? '(:a :b :c))
		     true)
		  ```
	- [[(list?)]]
		- ``` clojure
		  (= (list? '(:a :b :c))
		     true)
		  ```
- ---
- [[Countable]] operations
	- [[(count)]]
		- ``` clojure
		  (= (count '(:a :b :c))
		     3)
		  ```
	- [[(empty?)]]
		- ``` clojure
		  (= (empty? '())
		     true)
		  
		  (= (empty? '(:a :b :c))
		     false)
		  ```
	- [[(first)]]
		- ``` clojure
		  (= (first '(:a :b :c))
		     :a)
		  ```
	- [[(last)]]
		- ``` clojure
		  (= (last '(:a :b :c))
		     :c)
		  ```
	- [[(nth)]]
		- ``` clojure
		  (= (nth '(:a :b :c)
		          2)
		     :c)
		  ```
	- [[(second)]]
		- ``` clojure
		  (= (second '(:a :b :c))
		     :b)
		  ```