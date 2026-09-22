# Apply

The main use of `apply` is when you need to pass a whole collection as arguments to a function, instead of listing the arguments one by one.

A simple example with `max` (which compares its arguments and returns the largest):

```clojure
(apply max [1 2 3 4 5]) ;; 5

(max 1 2 3 4 5) ;; 5

;; The function is not applied correctly
;; because the vector is seen as a
;; single parameter!
(max [1 2 3 4 5]) ;; [1 2 3 4 5]
```

You can say that `apply` literally *applies* a collection as arguments to a function, which is useful in many other cases too!

It shines when you already have a vector and want to treat it as a list of arguments.

---

Liked `apply`? Our last topic: building a tiny HTTP server with Clojure.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/projeto/http.md">Next -> Mini HTTP server</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
