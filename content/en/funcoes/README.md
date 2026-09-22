# Functions

When we talk about functions we are talking about most of what a functional language does: *almost everything* is a function. A simple analogy: a box that takes an input, does some work inside, and returns an output.

![Black-box function example](https://www.researchgate.net/publication/230646848/figure/fig4/AS:669409437823002@1536611055840/Black-Box-function.png)

That is the idea. How do we declare a function in Clojure?

```clojure
(defn greet []
  (println "Hello there!"))

(greet)

;; Result:
;;  Hello there!
;;  nil
```

The structure is:
- `(`: start of a list
- `defn`: we are declaring a function
- `[]`: arguments/parameters (none in this case)
- `(println "Hello there!")`: print the message "Hello there!"
- `)`: end of the list
- `(greet)`: *invoke* the function

Functions always look like this: parameters go in square brackets and are used in the body. Here is a simple function that adds two values:

```clojure
(defn sum [a b]
  (println (+ a b)))

(sum 1 2)

;; Result:
;;  3
;;  nil
```
> Remember that `nil` is just the return value of `println`!

In this shape we take two parameters, add them, and print the result.

What if we want multiple arities — different behavior depending on how many arguments we get? We can!

```clojure
(defn testing-arguments
  ([a] (println "Only one argument was sent!"))
  ([a b] (println "Two arguments were sent!")))

(testing-arguments 1) ;; Only one argument was sent!

(testing-arguments 1 2) ;; Two arguments were sent!
```

This is Clojure's way of handling functions that behave differently based on argument count!

What if we want unbounded arguments (like `+`)? Yes:

```clojure
(defn endless [& args]
  (println args))

(endless 1 2 3 4) ;; (1 2 3 4)
```

You receive a list of arguments and can work with each however you like! If you only care about the first one and still want to accept the rest:

```clojure
(defn endless-2 [first-arg & args]
  (println "The first argument was " first-arg "\nThe others are: " args))

(endless-2 1 2 3 4)

;; Result:
;;  The first argument was  1 
;;  The others are:  (2 3 4)
;;  nil
```

Here we only treat the first argument; the rest stay as a list! To treat the second as well you could write `[first-arg second-arg & args]`, and so on!

---

Great! With the basics of functions in place, we can move to something a bit magical: recursion!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/funcoes/recursividade.md">Next -> Recursion</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
