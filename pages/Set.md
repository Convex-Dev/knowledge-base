alias:: [[Sets]]

- ---
- Unordered [[Collection]] of unique [[Values]]
- Meaning a [[Value]] can be present at most once
- Conceptually, akin to a [[Map]] where [[Keys]] point to themselves
- ---
- Create a new [[Set]] from scratch
	- Literal notation
		- Any number of [[Values]] in between `#{ }`
		- Commonly separated by space
			- `,` is also legal but not widely used unless it improves readability
		- ``` clojure
		  #{}
		  
		  #{1 :a \a ["Convex"]}
		  ```
	- [[(hash-set)]]
- ---
- Test if a [[Set]] contains a [[Value]]
	- By using it as a [[Function]]
		- ``` clojure
		  (= (#{:a :b} :a)
		     true)
		  
		  (= (#{:a :b} :c)
		     false)
		  ```
	- [[(contains-key?)]]
		- ``` clojure
		  (= (contains-key? #{:a :b}
		                    :a)
		     true)
		  
		  (= (contains-key? #{:a :b}
		                    :c)
		     false)
		  ```
	- [[(get)]]
		- ``` clojure
		  (= (get #{:a :b}
		          :a)
		     true)
		  
		  (= (get #{:a :b}
		          :c)
		     false)
		  
		  (= (get #{:a :b}
		          :c
		          :not-found)
		     :not-found)
		  ```
- Create new [[Sets]] by appending [[Values]] or other [[Collections]]
	- [[(assoc)]]
		- ``` clojure
		  (= (assoc #{:a :b}
		            :c
		            true)
		     #{:a :b :c})
		  
		  (= (assoc #{:a :b}
		            :a
		            true)
		     #{:a :b})
		  ```
	- [[(conj)]]
		- ``` clojure
		  (= (conj #{:a :b}
		           :c)
		     #{:a :b :c})
		  
		  (= (conj #{:a :b}
		           :a)
		     #{:a :b})
		  ```
	- [[(into)]]
		- ``` clojure
		  (= (into #{:a :b}
		           [:c :d])
		     #{:a :b :c :d})
		  
		  (= (into #{:a :b}
		           [:c :d :a :a :a :b :c :d :d])
		     #{:a :b :c :d})
		  ```
- Create new [[Sets]] by removing [[Values]]
	- [[(assoc)]]
		- ``` clojure
		  (= (assoc #{:a :b}
		            :a
		            false)
		     #{:b})
		  
		  (= (assoc #{:a :b}
		            :c
		            false)
		     #{:a :b})
		  ```
	- [[(disj)]]
		- ``` clojure
		  (= (disj #{:a :b :c}
		           :a)
		     #{:b :c})
		  
		  (= (disj #{:a :b :c}
		           :d)
		     #{:a :b :c})
		  ```
	- [[(empty)]]
		- ``` clojure
		  (= (empty #{:a :b})
		     #{})
		  ```
	- [[(filter)]]
		- ``` clojure
		  (= (filter (fn [x]
		               (>= x 0))
		             #{1 42 0 -42 -100})
		     #{1 0 42})
		  ```
- [[Set]] operations
	- [[(difference)]]
		- ``` clojure
		  (= (difference #{:a :b :c}
		                 #{:c :d})
		     #{:a :b})
		  
		  (= (difference nil
		                 #{:a :b})
		     #{}KKk)
		  ```
	- [[(intersection)]]
		- ``` clojure
		  (= (intersection #{:a :b :c}
		                   #{:b :c :d})
		     #{:b :c})
		  
		  (= (intersection nil
		                   #{:a :b})
		     #{})
		  ```
	- [[(subset?)]]
		- ``` clojure
		  (= (subset? #{:a :b}
		              #{:a :b :c})
		     true)
		  
		  (= (subset? #{}
		              #{:a :b})
		     true)
		  
		  (= (subset? #{:a :b}
		              #{:b :c :d})
		     false)
		  ```
	- [[(union)]]
		- ``` clojure
		  (= (union #{:a :b}
		            #{:b :c :d})
		     #{:a :b :c :d})
		  
		  (= (union #{:a :b}
		            nil)
		     #{:a :b})
		  ```
- [[Predicates]]
	- [[(coll?)]]
		- ``` clojure
		  (= (coll? #{:a :b})
		     true)
		  ```
	- [[(set?)]]
- [[Countable]] operations
	- [[(count)]]
		- ``` clojure
		  (= (count #{:a :b :c})
		     3)
		  ```
	- [[(empty?)]]
		- ``` clojure
		  (= (empty? #{})
		     true)
		  
		  (= (empty? #{:a :b :c})
		     false)
		  ```
	- [[(first)]]
		- ``` clojure
		  (= (first #{:a :b :c})
		     :c)
		  ```
	- [[(last)]]
		- ``` clojure
		  (= (last #{:a :b :c})
		     :b)
		  ```
	- [[(nth)]]
		- ``` clojure
		  (= (nth #{:a :b :c}
		          2)
		     :b)
		  ```
	- [[(second)]]
		- ``` clojure
		  (= (second #{:a :b :c})
		     :a)
		  ```
- Miscellaneous operations
	- [[(next)]]
		- ``` clojure
		  (= (next #{:a :b :c})
		     [:a :b])
		  ```