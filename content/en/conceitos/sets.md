# Sets

Sets are like mathematical sets — unordered and without duplicates. They are great for checking efficiently whether a collection contains an element, or for removing an arbitrary element.

You can define a set like this:

```clojure
#{1 2 3 4 5}
```

The output matches what you sent. Sets also refuse duplicates! If you try `#{1 2 3 4 5 1}` you get an error saying key `1` is duplicated!

Let's define a set for the next examples:

```clojure
(def set-developers
    #{"Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício"})
```

## Set?

To check whether something is a set, use `set?`!

```clojure
(set? set-developers)
```

The output is `true`, because it really is a set! If you run `(set? list-developers)` you get `false`!

## Contains?

To check whether a value exists in a set we have two options, starting with `contains?`!

```clojure
(contains? set-developers "Daniel")
```

The output is `true`, because `"Daniel"` is in the set! `(contains? set-developers "Guto")` returns `false`!

We can also look it up like this:

```clojure
(set-developers "Daniel")
```

Here the output is `"Daniel"`, and `(set-developers "Guto")` returns `nil`! Why does this work?

Remember that sets are hashed collections? The value you pass is the key. If the set finds it, it returns that value; if not, it returns nil!

## Keywords

We can also declare a set of keywords, with the syntax `:keyword`! A keyword's value is itself, so it behaves a bit differently from strings...

If you try something like `("Guto" set-developers)` you will not get `nil` — you will get an error! With keywords that does not happen: you can put the keyword before or after the set, as below:

```clojure
(def letters #{:a :b :c})

(:a letters) ;; :a

(letters :a) ;; :a

(:d letters) ;; nil
```

## Conj

We can still use `conj` to add an item to a set:

```clojure
(conj set-developers "Guto")
```

The output is `#{"Canhassi" "Kalane" "Daniel" "Fabrício" "Guto" "Cherry"}`, with the new value included!

## Disj

To remove an item from a set, use `disj`:

```clojure
(disj set-developers "Fabrício")
```

The output is `#{"Canhassi" "Kalane" "Daniel" "Cherry"}`. If the value is not there, you simply get the set back — no error.

---

How were sets? Let's look at maps.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/conceitos/mapas.md">Next -> Maps</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
