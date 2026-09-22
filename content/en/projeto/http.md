# Mini HTTP server

In this last topic we will build a simple HTTP server step by step so you can see how straightforward it is! The goal is to show project management with [Leiningen](https://leiningen.org/) and a bit of what a real project looks like.

A finished copy of this example lives in [`content/projeto/http-simples/`](https://github.com/lanjoni/clojure4noobs/tree/main/content/projeto/http-simples) (shared by both language versions of the tutorial).

## Creating your project

First, create a project named `http-simples`:

```sh
$ lein new app http-simples
```
> `app` is the template we want! Run `lein help new` to learn more!

Once the project is created, the structure will look similar to this:

```
.
├── CHANGELOG.md
├── LICENSE
├── README.md
├── doc
│   └── intro.md
├── project.clj
├── resources
├── src
│   └── http_simples
│       └── core.clj
└── test
    └── http_simples
        └── core_test.clj
```

The `test` directory is for your app's tests, `src` holds the source code, and `doc` is for documentation!

You also get a `README.md`, a `LICENSE` (project licensing), and a `CHANGELOG.md` (a log of version changes).

## Adding a dependency

To change project settings and add [http-kit](https://github.com/http-kit/http-kit) (a kit for spinning up an HTTP server easily), open `project.clj`. It looks something like this:

```clojure
(defproject http-simples "0.1.0-SNAPSHOT"
  :description "FIXME: write description"
  :url "http://example.com/FIXME"
  :license {:name "EPL-2.0 OR GPL-2.0-or-later WITH Classpath-exception-2.0"
            :url "https://www.eclipse.org/legal/epl-2.0/"}
  :dependencies [[org.clojure/clojure "1.11.1"]]
  :main ^:skip-aot http-simples.core
  :target-path "target/%s"
  :profiles {:uberjar {:aot :all
                       :jvm-opts ["-Dclojure.compiler.direct-linking=true"]}})
```

To add our dependency, change the `:dependencies` bit like this:

```clojure
;; ...
  :dependencies [[org.clojure/clojure "1.11.1"]
                 [http-kit "2.7.0"]]
;; ...
```
> We will use version `2.7.0`!

Done! Dependencies are declared. To download them, run:

```sh
$ lein deps
```

Nice!

## Defining the server

Time to define our web server! Open `src/http-simples/core.clj`. First we *require* `http-kit` by changing the namespace:

```clojure
(ns http-simples.core
  (:require [org.httpkit.server :refer [run-server]]))
```
> Those would be the first two lines of the project!

Now we create a function called `app` that handles routing and responses:

```clojure
(defn app [req]
  {:status  200
   :headers {"Content-Type" "text/html"}
   :body    (str "May the source be with you, He4rt Developers <3")})
```

We are not inspecting the request type here! We just prepare the server to accept GET requests (by default) at the root (`/`)! The body has a greeting — customize it however you like. You can also change `"Content-Type"` as needed.

We start the server in `-main` (the entry point) using `run-server` from `http-kit`, with `app` handling incoming requests:

```clojure
(defn -main [& args]
  (run-server app {:port 3000})
  (println "Server started on port 3000"))
```

Our server is ready!

## Running it

Go back to the project root and run:

```sh
$ lein run
```

You should see the message that the server started! Open your browser and visit `localhost:3000`!

<p align="center">
  <img src="https://media.giphy.com/media/S5Pt1ec834VWas7XGK/giphy.gif" width="280" alt="Calcifer burning happily">
  <br>
  <em>Calcifer is keeping your server warm on port 3000.</em>
</p>

---

See how elegant an HTTP server can be in Clojure? Time to wrap up.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/finalizacao/README.md">Next -> Wrap-up</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
