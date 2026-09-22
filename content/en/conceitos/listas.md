# Lists

Lists are sequential linked lists that add new elements at the **front**, not at the end like vectors. Their syntax uses parentheses around the items.

In fact, as we said earlier, our whole program is made of lists. In most cases the first item is a function. That is not unique to Clojure — it is how Lisp-family languages work.

## Working with lists

List handling is a bit different. Try the code below in your REPL.

```clojure
(1 2 3 4 5)
```

You got an error, right? The reason is simple: Clojure *thought* `1` was a function and the rest were arguments. To actually *see* the list we add a single quote at the front, telling Clojure not to treat the following list as a function call — we prevent it from being *evaluated* (you will see the term [evaluation](https://homepages.inf.ed.ac.uk/stg/NOTES/node71.html) a lot).

```clojure
'(1 2 3 4 5)
```

Now the output is the expected `(1 2 3 4 5)`. We can also use `list` to create a list.

```clojure
(list 1 2 3 4 5)
```
> This function declares a list whose contents are the arguments you pass.

Let's define a list for the examples below.

```clojure
(def list-developers
    '("Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício"))
```

We can use other functions on this list, such as `count`.

```clojure
(count list-developers)
```

The return value is `5`, because we declared 5 items!

## First

How do we get the first item? With `first`!

```clojure
(first list-developers)
```

The output is `"Kalane"`, the first item of our list!

## Rest

And the remaining items, skipping the first, just like with vectors? We use `rest`!

```clojure
(rest list-developers)
```

The output is `("Daniel" "Cherry" "Canhassi" "Fabrício")`!

## Nth

What if we want a specific index, like with vectors? Yes!

```clojure
(nth list-developers 3)
```
> The output would be `"Canhassi"`!

But could we then do this (as with vectors)?

```clojure
(list-developers 3)
```

No! If you ran that snippet you probably hit an error. With lists we cannot use indexes the same way we do with vectors...

## Conj

Remember that with vectors we can add items at the beginning or the end? With lists, `conj` adds only at the **front**!

```
(conj list-developers "Guto")
```

The output is `("Guto" "Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício")`!

---

How were lists? Ready to look at sets?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/conceitos/sets.md">Next -> Sets</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
