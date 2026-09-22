# Map

Imagine you have a collection of values and you want to apply an *effect* to every element — *map* a function over all of them and get a list of results.

For that job, `map` is your best friend! A simple example:

```clojure
(map inc [1 2 3 4 5])

;; Result:
;;  (2 3 4 5 6)
```

We applied `inc` (adds `1` to each value) to every element of the collection and got a list back.

We can also use anonymous functions:

```clojure
(map (fn [n] (* n 2)) [1 2 3])

;; Result
;;  (2 4 6)
```

Another way to do the same calculation without *declaring* an anonymous function with `fn`:

```clojure
(map #(* % 2) [1 2 3])

;; Result
;;  (2 4 6)
```

`#` starts a short *anonymous function*, and `%` is the argument passed in. Even shorter!

---

How was `map`? Let's look at `filter`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/manipulacoes/filter.md">Next -> Filter</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
