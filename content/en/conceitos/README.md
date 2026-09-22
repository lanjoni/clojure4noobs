# Concepts

Now we will cover some ideas that really matter for working with Clojure. One of them is:

> **Functions** are first-class citizens, so they get special treatment.

We could say that almost everything in Clojure is a function, and combining them (or not) produces some data. We can also say that in Clojure **data is first-class too**. Data is just data: Clojure does not (and does not care to) work with *types* the way many other languages do.

Clojure is not about type theory. It is a language that works directly with data in a simple way. That is a bit philosophical, and it is very much how people think about Clojure.

## Syntax

Yes, this moment has arrived... Time to understand Clojure syntax a bit better. Open your REPL with `lein repl` and let's try a few things!

The first visual cue is parentheses marking the start of a form. You can simplify the syntax as:

```clj
(function arg1 arg2 arg3 ...)
```

When you open parentheses you *tell* Clojure you are starting a function. In Lisp terms, that is a list whose first item is the function name, followed by its arguments, plus whatever should be done with those arguments (as we mentioned earlier).

A nice example is addition: the operator is prefix, not infix (where the sign sits between the arguments). See:

```clj
user=> (+ 1 2 3 4 5)
15
```

The function was called with a list of numbers to add! Technically, it is **always** like this. You pick a function and pass as many arguments as it expects (here it takes an unbounded list and adds them in order).

Why? Because it is simpler. It may feel new, but it is practical: you do not worry about operator order. You add a function, then its arguments. If an argument is another function, wrap it in parentheses. Here is `(6 + 2)/2`:

```clj
user=> (/ (+ 6 2) 2)
4
```

No matter the expression, the order is always the same. Everything is a function, so it gets simpler with practice! It feels weird at first, but you will get used to it.

## "*Variables*"

Variables are a special topic in Clojure. Can we even *call it a variable* if it does not vary? By default Clojure implements them (see [Vars](https://clojure.org/reference/vars) in the official docs) as immutable bindings: you bind a value to a name (a bit like a function with no parameters that returns something). For ease of learning, we will keep calling them variables, okay?

You define them with `def`, as in:

```clj
(def community "He4rt")
```

Now let's print a message with `println`:

```clj
user=> (println "Hello" community "!")
Hello He4rt !
nil
```
> Do not worry about that `nil`. It only means the function's return value is null (it was just printing). In Clojure every function returns something, even if that something is `nil`!

We just passed a list of arguments to `println` and our message was printed. Nice!

---

How was that first look at Clojure's core ideas?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/conceitos/estruturas.md">Next -> Data structures</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
