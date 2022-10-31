- Transformation of [[Data]] into [[Data]]
- By executing [[Macros]] it refers to
- Until the output does not refer to any [[Macro]] anymore
- ---
- ``` clojure
  ;; Note: `when` is a macro that expands to `cond`
  
  (= (expand '(when (< a b)
                :ok))
     '(cond
        (< a b) (do :ok)
        nil))
  ```