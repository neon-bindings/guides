---
layout: guide
title: The Neon Project - Hello, World!
nav-title: Hello, World!
nav-order: 1
---

# Hello, World!

This guide will walk you through writing, building, and running your first Neon project.

For our first Neon project, we'll write a tiny module that does nothing more than expose the functionality of an existing Rust crate. As simple as this is, it already demonstrates some of the usefulness of Neon: Rust's [crate ecosystem](https://crates.io/) is younger than npm, but growing quickly and already full of useful and unique libraries.

Our running example will use [Sean McArthur](http://seanmonstar.com/)'s [num_cpus](https://crates.io/crates/num_cpus) library, which returns the number of CPUs available on the current machine.

# Creating a New Project

The first thing we have to do is create a Neon project:

```shell
$ neon new num-cpus
```

This will ask us a series of questions similar to the ones asked by `npm new`. When it completes, the tool will have created a `num-cpus` directory with the following layout:

```text
num-cpus/
├── .gitignore
├── README.md
├── lib/
│   └── index.js
├── native/
│   ├── Cargo.toml
│   └── src/
│       └── lib.rs
└── package.json
```

The first thing to notice about this layout is that **a Neon project is a Node package**. In other words, the way to think of a Neon project is:

> Node on the outside, Rust on the inside.

# Building and Running

We haven't yet implemented anything, but just to see that `neon new` produces a complete, minimal Neon project, let's try building and running it.

```shell
$ neon build
neon info forcing rebuild for new build settings
# more compiler output...
neon info generating native/index.node
$ node
> require('.')
hello node
{}
```

# Adding a Rust dependency

The next thing to notice about our `num-cpus` project layout is that the Rust implementation lives in the `native/` subdirectory. This is where the `Cargo.toml` manifest file for your Rust code lives.

```toml
num_cpus = "1.4"
```

```shell
$ cd native
$ cargo update
```

# Try it Out!

```shell
$ node
> var numCPUs = require('.')
> numCPUs()
2
```

