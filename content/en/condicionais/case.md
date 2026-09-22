# Case

`case` is a bit different from `cond`. It is closer to `switch`/`case` in other languages: it matches *whole* values and has an extra clause for when none of the others match!

See the example below — it should click:

```clojure
(let [n 10]
  (case n
    1 "One ring!"
    2 "Two towers!"
    3 "Three laws of robotics!"
    4 "Fourth wall broken!"
    "It's over nine thousand!"))

;; Result:
;;  "It's over nine thousand!"
```
> We did not use `println` here, so the result is just a `string`!

With `case` we can list several cases and, at the end, add what other languages call a `default` for when nothing above matched!

---

Nice! That wraps up this chapter. Next: iteration, the famous *loops*.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/repeticao">Next -> Iteration</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
