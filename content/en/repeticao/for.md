# For

Loved by many, disliked by some, `for` is a classic loop. In most languages it looks something like:

```javascript
for (init; until; step){
  // Do something
}
```
> The shape of a `for` depends on the language, of course. The syntax does not always tell you exactly what it does!

Clojure's `for` looks different. Let's look at an example:

```clojure
(for [i (range 10)]
      (println i))
```

This prints the values from `0` to `9` (the given `range`) as a list. Clojure's `for` is similar to languages that iterate over collections. Here is another example using a vector:

```clojure
(def numbers [0 1 2 3 4 5 6 7 8 9])

(for [i numbers]
      (println i))
```

The result matches the `range` example, but this time we walk the whole vector. We could use `strings` and, instead of `println`, use `str` to concatenate, avoiding that extra printed return. See:

```clojure
(def letters ["a" "b" "c" "d" "e"])

(for [l letters]
      (str l))

;; Result:
;;  ("a" "b" "c" "d" "e")
```

You get a list of those letters, which is useful when you want a new list from a vector (or similar). Nice, right?

There is much more you can do with `for`. If you are curious, check the [ClojureDocs](https://clojuredocs.org/clojure.core/for) page!

---

Enjoyed `for`? Next up: `doseq`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/repeticao/doseq.md">Next -> Doseq</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
