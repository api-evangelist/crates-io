---
title: "Rust Function Overloading - Call for Experimentation"
url: "https://blog.rust-lang.org/inside-rust/2026/08/19/overloading-experiment/"
date: "2026-08-19"
author: "teor"
feed_url: "https://blog.rust-lang.org/inside-rust/feed.xml"
---
In partnership with the Rust Foundation's Rust-C++ Interop Initiative , the Rust Project has been experimenting with function overloading for FFI bindings . This experiment is now at a stage where compiler and interop tool developers can start exploring function overloading. Stable Rust already supports a form of overloading using tuples and traits , but calling these overloaded functions looks strange, because the overloaded arguments have to be passed as a single tuple argument, like this: hypot((2.0, 3.0, 6.0)) .
