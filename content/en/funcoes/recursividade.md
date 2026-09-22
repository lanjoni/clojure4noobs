# Recursion

Borrowing the definition from José Romildo Malaquias (Chapter 6 of his Functional Programming course at the Federal University of Ouro Preto), translated here:

> Recursion is the programming mechanism in which a function (or other object) is defined in terms of itself. A recursive function is a function defined in terms of itself.

> **Recursion**: see *Recursion*. If you want the official word, the [Clojure special forms reference](https://clojure.org/reference/special_forms#recur) has your back.

<p align="center">
  <img src="https://media.giphy.com/media/buiddJIVvHHXReeJbe/giphy.gif" width="220" alt="Soot sprites carrying coal one after another">
  <br>
  <em>One sprite calls the next, who calls the next, who calls the next...</em>
</p>

Roughly: when we see *recursion*, a function calls a subroutine that happens to be itself — an infinite-looking idea applied to something finite (deep, right?).

A fun example is counting backwards (you will see why this matters in a moment):

```clojure
(defn countdown [n]
  (println n)
  (if (pos? (dec n))
    (countdown (dec n))))

(countdown 10)
```

This counts from `10` down to `1` (a proper rocket launch countdown), then returns `nil` because of `println`. We print the current number; then `pos?` returns `true` if the number is greater than `0`. If so, we call `countdown` again with `n - 1` (`dec` subtracts one, similar to `i -= 1` in other languages).

Another way is to use `recur` instead of calling `countdown` by name:

```clojure
(defn countdown-recur [n]
  (println n)
  (if (pos? (dec n))
    (recur (dec n))))

(countdown-recur 10)
```

The result is the same, but `recur` is interesting: it sets up a recursive call more efficiently, without extra stack frames!

Running `(doc recur)` shows:

```clojure
-------------------------
recur
  (recur exprs*)
Special Form
  Evaluates the exprs in order, then, in parallel, rebinds
  the bindings of the recursion point to the values of the exprs.
  Execution then jumps back to the recursion point, a loop or fn method.

  Please see http://clojure.org/special_forms#recur
```

---

How was recursion? Ready for `multimethods`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/funcoes/multimethods.md">Next -> Multimethods</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
