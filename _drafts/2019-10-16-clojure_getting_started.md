---
layout: post-comments
title:  "Clojure: Hello World! Creating a project [quick] [steps]"
//date:   
excerpt: Something Something
description: Because there is no such a thing as too many Getting Started
image: /images/polite-code-reviewer/buddha-try-to-not-be-an-asshat.jpg
categories:
  - en
  - tutorial
  - clojure
tags:
  - lisp
  - functional-programming
  - clojure
  - getting-started
  - quick
  - tutorial
  - steps
---

### TL;DR

For the very bare minimun - no dependencies required - "hello world",
follow the steps below.

If you want a more standard project skeleton out of this tutorial,
skip to [this not so short session](){: target="blank"}.

#### Steps

  - `$ brew install clojure` ([not on MacOS?](https://clojure.org/guides/getting_started){: target="blank"})
  - `$ mkdir -p tutorial/src`
  - Create and edit a clojure file: `tutorial/src/hello_world.clj` to:
	  - create the _hello-world_ namespace so we can refer to it when executing the app
	- print the obligatory hello world from the `-main` function (entry point)

```clj
(ns hello-world)
(defn -main []
  (prn "hello world"))
```

  - `$ clj -m hello-world` to run the program indicating that `hello-world` is the entry point namespace

```
➜ clj -m hello-world
"hello world"
```

### A little bit more detailed

Install Clojure if you have not done it yet.
I am on a MacOS and I used _brew_:

  - `$ brew install clojure`

If you are in a different operation system
go real fast and
[follow the official docs](https://clojure.org/guides/getting_started){: target="blank"}
for the installation, then come back here, please.

Now create a directory for your brand new project.
On my example it will be called `started`:

  - `$ mkdir started`

This is a Clojure language "hello world" type of getting started.

> Why though?

And a very appropriate answer is:

And there is also a little rationale for why I am writting these
in case the reader is interested
[in those sort of shenanigans](/writting-to-myself){: target="blank"}.

Besides that I felt that the Google search results for
"clojure getting started" were too bloated for my own taste.
Seemed a little hard for a novice like myself to _just follow_
and go further from there.

Granted I also suffer from a lack of capacity to retain information
on the fast access area of the ol'brain.

Let's start.

#### Basic project

Install Clojure if you have not done it yet.
I am on a MacOS and I used _brew_:

  - `$ brew install clojure`

If you are in a different operation system
go real fast and
[follow the official docs](https://clojure.org/guides/getting_started){: target="blank"}
for the installation, then come back here, please.

  - `$ mkdir -p tutorial/src`
  - Create and edit `tutorial/deps.edn` and add:
    - the clojure version you are working on (I am using _clojure-1.10.1_ right now):

```edn
{
  :deps {
         org.clojure/clojure {:mvn/version "1.10.1"}
  }
}
```

  - `$ clj -A:new app PREFIX/your_project_name`
    - The name should be fully qualified (WHY, though?)
  - `$ cd your_project_name-test`
  - `$ clj -A:test:runner`

```
... if any dependency need to be downloaded, it will be done here
Running tests in #{"test"}

Testing PREFIX.your_project_name-test

FAIL in (a-test) (your_project_name_test.clj:7)
FIXME, I fail.
expected: (= 0 1)
  actual: (not (= 0 1))

Ran 1 tests containing 1 assertions.
1 failures, 0 errors.
```

    - This means everything is working!

  - Remove test/
  - Create your first file: `src/PREFIX/hello.clj`

```clj
(ns PREFIX.hello
  (:gen-class))

(defn hello
  [name]
  (str "hello " name))
```

  - Create your first test file: `test/PREFIX/hello_test.clj`

```clj
(deftest test-this
  (testing "Hello World"
    (is (= "hello world" (hello "world")))))
```

    - the function should be called test-* (Why though?)
  - `$ clj -A:test:runner`

```
Running tests in #{"test"}

Testing PREFIX.hello-test

Ran 1 tests containing 1 assertions.
0 failures, 0 errors.
```

### References

  - https://github.com/clojure/tools.deps.alpha
  - https://github.com/clojure/tools.deps.alpha/wiki/Tools
  - https://github.com/seancorfield/clj-new
