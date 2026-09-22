# Introduction 

<p align="center">
  <img src="https://media.giphy.com/media/omHPYZttAVAAw/giphy.gif" width="320" alt="Studio Ghibli characters walking together">
  <br>
  <em>Grab your backpack — the journey starts here.</em>
</p>

## What is Clojure?

<img align="right" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/clojure/clojure-original.svg" alt="Language logo" width="100">

### History

Clojure is a programming language created in 2007 by [Rich Hickey](https://github.com/richhickey). It belongs to the Lisp family, treats functions as first-class values, emphasizes immutable data, and runs on the Java Virtual Machine (the well-known JVM). It can also run in other environments, such as Clojure CLR (compiling to .NET) and ClojureScript (compiling to JavaScript).

- **Okay, but where did the idea come from?**

Before Clojure, Rich worked on *dotLisp*, a similar project for the .NET platform. He also built **jfli** (a bridge from Java to Common Lisp), **FOIL** (a foreign object interface for Lisp), and **Lisplets** (a Lisp-friendly interface for Java Servlets), exploring interoperability between Lisp and Java.

After about two years of full-time work on Clojure, Rich was finally able to announce the language to the Common Lisp community.

### Philosophy

The main goal was to build a modern Lisp for functional programming, running on the JVM and designed for concurrent computation.

In Lisp as a whole — and Clojure is no exception — almost everything looks like a list: the first item is the *function*, followed by its arguments, describing the work to be done.

An important part of Clojure's design is stability: it aims to be production-ready. Running on the JVM is a bonus, with all the extra machinery that a virtual machine provides.

In the paper [A History of Clojure](https://dl.acm.org/doi/pdf/10.1145/3386321), Rich Hickey walks through several aspects of the language, highlighting how stable its line count has been over time.

![Clojure lines of code](https://github.com/lanjoni/clojure4noobs/blob/main/.github/clojure_lines_of_code.png)

In the chart above you can see that stability over the years: a Clojure app built on one version will *almost* always still run years later on a more recent release, without much extra work.

## Where do we see Clojure?

It is used by companies such as Walmart, Accenture, Mercado Livre, SoundCloud, and Puppet Labs. Support is provided by Cognitect, which is now part of Nubank (yes, Nubank uses Clojure)!

The first public release of Clojure appeared in 2007, and the first stable release in 2009. At the time of writing we are on version 1.11.1 (April 5, 2022)!

---

Like Clojure so far? Shall we install it and try our first experiments?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/content/en/intro/instalacao.md">Next -> Installation</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
