# Documentation

You can read docs for specific Clojure functions right from your code, using a function called `doc`.

## Doc

With this function you can read documentation for any Clojure function, with a description of how it works — handy while you develop.

A simple example is `+`, which adds numbers. To see its docs, run:

```clojure
(doc +)
```

You will get something like:

```
clojure.core/+
([] [x] [x y] [x y & more])
  Returns the sum of nums. (+) returns 0. Does not auto-promote
  longs, will throw on overflow. See also: +'
nil
```
> As we said before, `nil` is just the function's return value.

## Find-doc

If you need to search for some action — a string that appears in the docs but you cannot remember the function name — `find-doc` helps. See:

```clojure
(find-doc "sum of nums")
```

You might get:

```
-------------------------
clojure.core/+
([] [x] [x y] [x y & more])
  Returns the sum of nums. (+) returns 0. Does not auto-promote
  longs, will throw on overflow. See also: +'
-------------------------
clojure.core/+'
([] [x] [x y] [x y & more])
  Returns the sum of nums. (+') returns 0. Supports arbitrary precision.
  See also: +
nil
```

It searches Clojure's documentation for functions whose description contains the string you passed.

## Apropos

If you already have an idea of the function name (or part of it) and want functions whose names contain that text, `apropos` is what you want.

Look for functions whose name contains a given snippet:

```clojure
(apropos "replace")
```

The result looks like:

```
(clojure.core/replace clojure.string/re-quote-replacement clojure.string/replace clojure.string/replace-first clojure.walk/postwalk-replace clojure.walk/prewalk-replace clojure.zip/replace)
```

## ClojureDocs

If you prefer an interactive web UI, I strongly recommend [ClojureDocs](https://clojuredocs.org/) — great for searching examples.

---

Enjoyed Clojure's built-in docs? Next: logic in Clojure.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/conceitos/logica.md">Next -> Logic</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
