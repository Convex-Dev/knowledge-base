alias:: Maps

- ---
- [[Associative]] [[Collection]]
	- Mapping [[Keys]] of any [[Types]]
	- To [[Values]] of any [[Types]]
- [[Key-Values]] are **not** [[Sequential]]
	- Order is stable but not predictable from a user perspective
- ---
- Create new [[Maps]] from scratch
	- Literal notation
		- Pairs of [[Key-Values]] in between `{ }`
			- ``` clojure
			  {}
			  
			  {:name   "Convex"
			   :status :awesome}
			  
			  {[:complex "key"] {:recursive 'value}}
			  ```
		- Pairs can be separated with `,` if it improves readability
			- ``` clojure
			  {:name "Convex", :status :awesome}
			  ```
	- [[(hash-map)]]
- ---
- Retrieve a [[Value]] by [[Key]]
	- Using [[Maps]] as [[Functions]]
		- ``` clojure
		  (= ({:a "a"} :a)
		     "a")
		  
		  (nil? ({:a "a"} :b))
		  
		  (= ({:a "a"} :b
		               :not-found)
		     :not-found)
		  ```
	- [[(get)]]
		- ``` clojure
		  (= (get {:a "a"}
		          :a)
		     "a")
		  
		  (nil? (get {:a "a"}
		             :foo))
		  
		  (= (get {:a "a"}
		          :foo
		          :not-found)
		     :not-found)
		  ```
	- [[(get-in)]]
		- ``` clojure
		  (= (get-in {:a {:b 42}}
		             [:a :b])
		     42)
		  
		  (nil? (get-in {:a {:b 42}}
		                [:foo :bar]))
		  
		  (= (get-in {:a {:b 42}}
		             [:foo :bar]
		             :not-found)
		     :not-found)
		  ```
- ---
- Create new [[Maps]] by adding [[Values]]
	- [[(assoc)]]
		- ``` clojure
		  (= (assoc {}
		            :a
		            "a")
		     {:a "a"})
		  
		  (= (assoc {:a "a"}
		            :b
		            "b")
		     {:a "a"
		      :b "b"})
		  ```
	- [[(assoc-in)]]
		- ``` clojure
		  (= (assoc-in {}
		               [:a :b]
		               42)
		     {:a {:b 42}})
		  
		  (= (assoc-in {:a {:b 42}}
		               [:a :c]
		               100)
		     {:a {:b 42
		          :c 100}})
		  ```
	- [[(into)]]
		- ``` clojure
		  (= (into {:a "a"}
		           [[:b "b"]
		            [:c "c"]])
		     {:a "a"
		      :b "b"
		      :c "c"}
		  ```
	- [[(merge)]]
		- ``` clojure
		  (= (merge {:a "a"
		             :b "b"}
		            {:c "c"
		             :d "d"})
		     {:a "a"
		      :b "b"
		      :c "c"
		      :d "d"})
		  ```
- ---
- Create new [[Maps]] by removing [[Values]]
	- [[(dissoc)]]
		- ``` clojure
		  (= (dissoc {:a "a"
		              :b "b"}
		             :a)
		     {:b "b"})
		  
		  (= (dissoc {:a "a"
		              :b "b"}
		             :c)
		     {:a "a"
		      :b "a"})
		  ```
	- [[(empty)]]
		- ``` clojure
		  (= (empty {:a "a"
		             :b "b"})
		     {})
		  ```
- ---
- [[Countable]] operations (order is not [[Sequential]] but it is stable)
	- [[(count)]]
		- ``` clojure
		  (= (count {:a "a"
		             :b "b"})
		     2)
		  ```
	- [[(empty?)]]
		- ``` clojure
		  (= (empty? {})
		     true)
		  
		  (= (empty? {:a "a"})
		     false)
		  ```
	- [[(first)]]
		- ``` clojure
		  (= (first {:a "a"
		             :b "b"})
		     [:a "a"])   
		  ```
	- [[(last)]]
		- ``` clojure
		  (= (last {:a "a"
		            :b "b"})
		     [:b "b"])
		  ```
	- [[(nth)]]
		- ``` clojure
		  (= (nth {:a "a"
		           :b "b"}
		          1)
		     [:b "b"])
		  ```
	- [[(second)]]
		- ``` clojure
		  (= (second {:a "a"
		              :b "b"})
		     [:b "b"])
		  ```
- ---
- [[Predicates]]
	- [[(coll?)]]
		- ``` clojure
		  (= (coll? {:a "a"
		             :b "b"})
		     true)
		  ```
	- [[(contains-key?)]]
		- ``` clojure
		  (= (contains-key? {:a "a"}
		                    :a)
		     true)
		  
		  (= (contains-key? {:a "a"}
		                    :b)
		     false)
		  ```
	- [[(map?)]]
- ---
- [[Map]]-specific operations
	- [[(keys)]]
		- ``` clojure
		  (= (keys {:a "a"
		            :b "b"})
		     [:a :b])
		  ```
	- [[(values)]]
		- ``` clojure
		  (= (values {:a "a"
		              :b "b"})
		     ["a" "b"])
		  ```
- ---
- Miscellaneous operations
	- [[(next)]]
		- ``` clojure
		  (= (next {:a "a"
		            :b "b"
		            :c "c"})
		     [[:a "a"] [:b "b"]])
		  ```