# Loop

You can think of `loop` as similar to `while`: while something is true, the instructions keep running!

See the example below:

```clojure
(loop [i 1]
  (when (<= i 10)
    (println i)
    (recur (inc i))))
```

This prints a count from `1` to `10`, then returns `nil`! `inc` adds `1` to `i`, like a counter (similar to `i += 1` in other languages).

At the end you need `recur` so the next pass runs with the updated binding of `i`, in a recursive way.

That is the basic shape of a `loop`!

<p align="center">
  <img src="https://media.giphy.com/media/WOfroaZcqVIc6rbN51/giphy.gif" width="240" alt="Soot sprite bouncing in place">
  <br>
  <em>Soot sprites: the original infinite loop.</em>
</p>

---

How were the iteration constructs? Which is your favorite? Next we will look at functions in Clojure.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/funcoes">Next -> Functions</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
