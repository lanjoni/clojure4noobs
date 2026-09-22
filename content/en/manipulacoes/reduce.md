# Reduce

Imagine mapping over a collection but returning a *single* result, built by combining values in sequence.

It sounds a bit complex, but it is practical. See:

```clojure
(reduce + [1 2 3 4])

;; Result:
;;  10
```

`reduce` was applied to that sequence, similar to `(+ 4 (+ 3 (+ 1 2)))`!

Another example, this time with a named function:

```clojure
(defn multiply [a b]
  (* a b))

(reduce multiply [1 2 3 4])

;; Result:
;;  24
```

Same idea, with a specific function. We can unpack it as: `1 * 2 = 2` → `2 * 3 = 6` → `6 * 4 = 24`! You apply it across a whole collection.

---

How was `reduce`? Practical, right? Next: `apply`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/manipulacoes/apply.md">Next -> Apply</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
