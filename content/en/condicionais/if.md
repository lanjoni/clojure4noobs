# If

You will find `if` in many languages. Its main job is to take a path when a condition is true, or an alternative path when it is not.

Clojure's `if` looks a bit different because everything is a function that takes arguments. A well-known `if` in other languages might look like:

```javascript
if (condition) {
  // Do something
} else {
  // Do something else
}
```

In Clojure it works a little differently:

```clojure
(if (> 1 2)
    (println "1 is greater than 2")
    (println "1 is not greater than 2"))

;; Return:
;;  1 is not greater than 2
;;  nil
```

The shape is easy to follow: `(if (condition) (then-branch) (else-branch))`, with inner functions for each branch.

We could go further:

```clojure
(def a 5)

(if (< a 0)
    (println "Less than 0")
    (if (= a 0)
        (println "Equal to 0")
        (println "Greater than 0")))

;; Return:
;;  Greater than 0
;;  nil
```

To simplify, we can use a local binding with *let*:

```clojure
(let [a 5]
  (if (< a 0)
    (println "Less than 0")
    (if (= a 0)
        (println "Equal to 0")
        (println "Greater than 0"))))

;; Return:
;;  Greater than 0
;;  nil
```

Here *let* binds a value to a *variable* in the same context — it stays in the scope where it was declared!

What if we want more than one expression in a branch? Use `do`:

```clojure
(if (> 1 2)
    (do
      (println "Beep boop, values received!")
      (println "Looks like 1 is greater than 2, Captain!"))
    (do
      (println "Beep boop, values received over here!")
      (println "Looks like 1 is not greater than 2, Captain!")))

;; Return:
;;  Beep boop, values received over here!
;;  Looks like 1 is not greater than 2, Captain!
;;  nil
```

---

What did you think of `if`? Let's meet `when`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/condicionais/when.md">Next -> When</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
