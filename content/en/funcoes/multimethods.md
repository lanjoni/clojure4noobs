# Multimethods

This is one of the nicest ideas in Clojure! Remember when we used `cond` to handle several conditions? `multimethods` do *almost the same thing*, but more elegantly!

See an example:

```clojure
;; We define an identity, stating
;; that we will have a `multimethod`
(defmulti factorial identity)

;; If factorial is called with
;; argument `0`, then
;; return 1
(defmethod factorial 0 [_]  1)

;; Otherwise (:default) we
;; compute factorial
;; recursively
(defmethod factorial :default [n]
  (* n (factorial (dec n))))

(factorial 0) ;; 1
(factorial 1) ;; 1
(factorial 3) ;; 6
```

This is a clearer way to declare how different methods should be handled. We only recurse when we need to (many factorial examples use an `if` for that check).

So the main goal of `defmethod` is to make those method-specific treatments easy to read.

---

Great! After `multimethods`, a very useful topic: anonymous functions!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/funcoes/funcoes_anonimas.md">Next -> Anonymous Functions</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
