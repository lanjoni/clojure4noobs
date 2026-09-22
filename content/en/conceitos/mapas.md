# Maps

Maps associate keys with values. Other languages often call them dictionaries or hash maps.

A map always pairs a key with a value. The basic syntax looks like this:

```clojure
{"a" "b" "c" "d"}
```

In the REPL you will see something like `{"a" "b", "c" "d"}`! The comma is how the map is printed internally: two keys and two values — key `"a"` → value `"b"`, key `"c"` → value `"d"`!

With maps it is common to use commas for that reason (they are optional), or to split across lines. You can also build a map with `hash-map`:

```clojure
(hash-map "a" "b" "c" "d")
```

The output is the same! Let's define a fixed map for our examples:

```clojure
(def songs {"The Imperial March" "John Williams"
            "Concerning Hobbits" "Howard Shore"
            "No Time for Caution" "Hans Zimmer"
            "Ghostbusters" "Ray Parker Jr."})
```

## Get

To look up a key we have two options. First, `get`:

```clojure
(get songs "Ghostbusters")
```

The output is `"Ray Parker Jr."`. We can also call the map with the key, as we saw before:

```clojure
(songs "Ghostbusters")
```

Same output!

## Assoc

We can add new key/value pairs with `assoc`: the map, then the key, then the value.

```clojure
(assoc songs "Duel of the Fates" "John Williams")
```

The output is the full map (items separated by commas) with the new pair added!

## Dissoc

We can remove a whole entry by key with `dissoc`!

```clojure
(dissoc songs "The Imperial March")
```

You get the full map without the `"The Imperial March"` key and value!

## Contains?

Check whether a map has a key with `contains?`!

```clojure
(contains? songs "Concerning Hobbits")
```

The output is `true`. Looking up `"Free Bird"` would return `false`!

## Find

Besides checking existence, we can fetch the key and value together with `find`!

```clojure
(find songs "No Time for Caution")
```

The output is `["No Time for Caution" "Hans Zimmer"]` — a vector! If the key is missing you get `nil`.

## Keys

To list every key, use `keys`!

```clojure
(keys songs)
```

The output is `("The Imperial March" "Concerning Hobbits" "No Time for Caution" "Ghostbusters")`.

## Vals

To list every value, use `vals`!

```clojure
(vals songs)
```

The output is `("John Williams" "Howard Shore" "Hans Zimmer" "Ray Parker Jr.")`.

## Zipmap

We can build a new map from a set with `zipmap`!

```clojure
(zipmap #{"a" "b" "c"} (repeat 1))
```

The return value is `{"a" 1, "b" 1, "c" 1}`: keys from the set, values from `(repeat 1)`!

## Merge

Combining maps is handy. `merge` joins two maps into a new one. First another map:

```clojure
(def new-songs {"Sweet Child O' Mine" "Guns N' Roses"
                    "Dream On" "Aerosmith"
                    "Hotel California" "Eagles"
                    "Come As You Are" "Nirvana"})
```

Then `merge`:

```clojure
(merge songs new-songs)
```
> You can use `merge-with` to define a rule when maps share the same keys!

The output is the combination of both maps!

---

Want more on maps? Next we will look at documentation in Clojure.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/conceitos/documentacoes.md">Next -> Documentation</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
