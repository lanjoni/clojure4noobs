# Leiningen <img align="right" src="https://leiningen.org/img/leiningen.jpg" alt="Leiningen logo" width="100">

Leiningen is a dependency manager with many features for building Clojure applications.

## How do I install it?

On the [official site](https://leiningen.org/) you will find an install script that works on any operating system. You can also install it with your favorite package manager, such as Homebrew on macOS.

For example, with Homebrew just run `brew install leiningen`!

## Using it

To create a new project with Leiningen, run:

```sh
$ lein new app test
```

> In this example we use the `app` template, but there are other templates too! Run `lein help new` to see the options!

With the project created you will notice a directory named `test` — the template worked. Go into that directory and you should see a structure similar to this:

```md
├── CHANGELOG.md
├── LICENSE
├── README.md
├── doc
│   └── intro.md
├── project.clj
├── resources
├── src
│   └── test
│       └── core.clj
├── target
│   └── test
│       └── stale
│           └── leiningen.core.classpath.extract-native-dependencies
└── test
    └── test
        └── core_test.clj
```

A few interesting files show up: `project.clj` lists project dependencies, `src/test/core.clj` is the "core" (what other languages often call `main` or the entry point), plus an automatically generated test directory.

Open the "core" file and let's see what it offers:

```clj
(ns test.core
  (:gen-class))

(defn -main
  "I don't do a whole lot ... yet."
  [& args]
  (println "Hello, World!"))
```

Notice that a `-main` is defined to run when we start the project! Run `lein run` and it will print "Hello, World!" Pretty nice, right?

Leiningen can do much more. Throughout this intro we will use it whenever we can!

## REPL

Yes, Leiningen ships a REPL (Read-Eval-Print Loop) for your projects. It is great for interactive testing and REPL-driven development (trust me: productivity jumps when the REPL becomes a friend)! Start it with `lein repl` and you should see something like this:

```sh
nREPL server started on port 49654 on host 127.0.0.1 - nrepl://127.0.0.1:49654
REPL-y 0.5.1, nREPL 1.0.0
Clojure 1.11.1
OpenJDK 64-Bit Server VM 19.0.2
    Docs: (doc function-name-here)
          (find-doc "part-of-name-here")
  Source: (source function-name-here)
 Javadoc: (javadoc java-object-or-class-here)
    Exit: Control+D or (exit) or (quit)
 Results: Stored in vars *1, *2, *3, an exception in *e

test.core=>
```

From the REPL you can import functions from your project, try things out, even define new functions and experiment. Cool, right?

---

Nice! That was our first look at Leiningen. Ready to learn some Clojure concepts?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/conceitos">Next -> Concepts</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
