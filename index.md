---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: guide
---

# Guides and Tutorials

Welcome to the Neon guides! This documentation should help you get up and running quickly, as well as learn useful techniques for making the most of Neon. If you're looking for reference material, you might want to try the [API documentation](https://api.neon-bindings.com/).

## What is Neon?

Neon is a library and toolchain for embedding [Rust](https://www.rust-lang.org/) in your [Node.js](https://nodejs.org) apps and libraries.

## Why Neon?

With Neon, you can create native Node modules like you might in C or C++, but with none of the fear and headaches associated with unsafe systems programming. Embedding Rust in Node can be useful for many reasons:

  * Raw performance
  * [Threads and parallel programming](./threads/)
  * Access to Rust's growing [package ecosystem](https://crates.io)
  * Access to native OS-specific libraries

Neon also works hard to make creating native modules _easy_, with a convenient command-line interface and workflow built around sensible project conventions. This eliminates a lot of the usual hassle of building native Node modules.

## Where do I Start?

The best place to go next is the [Getting Started](./getting-started/) guide, which will help you get Neon installed on your system. From there, try out the [Hello, World!](./hello-world/) guide to write your first native Node module with Neon!
