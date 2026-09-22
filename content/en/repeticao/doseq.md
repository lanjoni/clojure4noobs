# Doseq

This will probably be the shortest topic! `doseq` is simply a `for` that returns nothing!

See the example below:

```clojure
(def numbers [0 1 2 3 4 5 6 7 8 9])

(doseq [i numbers]
      (println i))

;; Result:
;;  1
;;  2
;;  3
;;  4
;;  5
;;  nil
```
> The last return (here `nil`) is the value returned by `doseq`!

Use it when you do not need a list-shaped return the way `for` gives you!

---

See? `doseq` is simple. Our last iteration construct is the famous `loop`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/repeticao/loop.md">Next -> Loop</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
