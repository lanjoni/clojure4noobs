# Filter

We know `map` applies a function to a collection and returns a list of results. What if we could *filter* a collection by a condition and get only the items that match?

That is the *main* job of `filter`. See:

```clojure
(filter odd? (range 1 21))

;; Result:
;;  (1 3 5 7 9 11 13 15 17 19)
```

`range` builds a collection of values from `1` up to (but not including) `21`, then `odd?` checks whether each number is odd. If it is, it goes into the result list; otherwise it is dropped.

Anonymous functions work the same way as with `map`. Here is a named function instead:

```clojure
(defn greater-than-3 [n]
  (> n 3))

(filter greater-than-3 (range 1 10))

;; Result:
;;  (4 5 6 7 8 9)
```

That is how we pass checks for `filter` to apply!

---

Liked `filter`? Next: `reduce`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/manipulacoes/reduce.md">Next -> Reduce</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
