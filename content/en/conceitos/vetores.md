# Vectors

Vectors are sequential, indexed structures — they have identifying indexes. If you have used other languages, you have probably met vectors or *arrays* already.

Clojure writes vectors with square brackets (nothing surprising). A vector of numbers looks like this:

```clojure
[1 2 3 4 5 6 7 8 9]
```
> You do not need commas. Just spaces between items.

You might be thinking: "okay, but you said Clojure treats data as plain data — can I mix types in a vector?" Yes!

```clojure
[1 2 3 true false "He4rt Developers"]
```
> Mixed types in the same structure are fine.

Let's define a fixed vector to play with. Feel free to pick your own values and indexes! Mine looks like this:

```clojure
(def developers
     ["Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício"])
```

## First

How do we get the first item? With `first`!

```clojure
(first developers)
```

The output is `"Kalane"`, because that is the first index of our vector!

## Rest

And how do we show the remaining items, skipping the first — similar to `tail` in other languages? We use `rest`!

```clojure
(rest developers)
```

The output is `("Daniel" "Cherry" "Canhassi" "Fabrício")`!

## Nth

What if we want a specific index? Possible — in two ways, and I will explain why...

```clojure
(nth developers 3)
```
> The output is `"Canhassi"`!

Or simply:

```clojure
(developers 3)
```
> The output is `"Canhassi"`!

The second form works because of something we said earlier: `def` is a bit like declaring a function that takes no extra arguments but still returns something. Same idea here!

## Count

To count how many values are in the vector, use `count`!

```clojure
(count developers)
```

The output is `5`, because we have 5 values!

## Conj

We can also add a new item with `conj`!

```clojure
(conj developers "Guto")
```

The output is `["Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício" "Guto"]` — the new item is added at the **end** of the vector!

## Cons

To add an element at the beginning of a vector's contents, use `cons`!

```clojure
(cons "Guto" developers)
```

The output is `("Guto" "Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício")`!

Notice something: we used several functions that "change" the vector and printed modified values, right? Let's look at `developers` after all that...

```clojure
(println developers)
```

You will see the original value, unchanged from when it was defined! As mentioned before, Clojure treats structures as immutable: it creates new values you can use however you want, without mutating the original. That is safer for your code!

---

Like how vectors work in Clojure? Next up: lists.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/conceitos/listas.md">Next -> Lists</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
