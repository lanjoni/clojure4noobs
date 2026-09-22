# Logic

When we talk about logic we are really talking about comparison. As we have seen, Clojure treats functions with prefix syntax across the board.

## =

Starting with `=`:

```clojure
(= 1 true) ;; false

(= 1 1) ;; true

(= true true) ;; true

(= 1 2) ;; false

(= 1 1 1) ;; true

(= 1 1 2) ;; false
```
> Important: `!=` does not exist here! If you try it you will get an error... Keep going and we will cover negation in Clojure!

Notice that `true` and `1` are *not* treated as the same thing here, which affects some comparisons! We can also compare three or more values to see if they are all equal. That works because of the syntax we discussed earlier, just like `+`.

## > >= < <=

Checking whether values are greater or smaller is useful, and Clojure makes it elegant:

```clojure
(< 1 2) ;; true

(<= 1 2) ;; true

(> 1 2) ;; false

(>= 1 2) ;; false

(< 1 2 3) ;; true

(< 1 3 2) ;; false
```

We can still pass more than two arguments. In the last example the result is `false` because the values are not strictly increasing: `1` is less than `3`, but `3` is not less than `2`!

## And

To check that every argument is truthy we use `and`, similar to `&&` in other languages:

```clojure
(and true true) ;; true

(and true false) ;; false

(and true true true) ;; true
```

Like the earlier functions, it checks each argument and returns whether the overall result is `true` or `false`.

## Or

To check that at least one argument is truthy we use `or`, similar to `||` in other languages:

```clojure
(or true true) ;; true

(or true false true) ;; true

(or false false) ;; false
```

A single true argument is enough for `true`, no matter how many arguments you pass!

## Not

`not` negates a condition, similar to `!` in other languages:

```clojure
(not false) ;; true

(not true) ;; false

(not (> 1 2)) ;; true
```

In the last example `(> 1 2)` would return `false` because `1` is not greater than `2`, but `not` flips it to `true`!

---

How was logic in Clojure? Next: conditionals.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/condicionais">Next -> Conditionals</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
