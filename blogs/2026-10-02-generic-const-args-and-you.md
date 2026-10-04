---
title: "Generic Const Args and You"
url: "https://blog.rust-lang.org/inside-rust/2026/10/02/generic-const-args-and-you/"
date: "2026-10-02"
author: "BoxyUwU"
feed_url: "https://blog.rust-lang.org/inside-rust/feed.xml"
---
Back in June of 2024 at RustFest Zürich, the Const Generics project group first discussed a new design for supporting more complex uses of generic parameters in Const Generics. Since then, we've continued to refine the initial design and have implemented the new design as a family of features dubbed "Generic Const Arguments" (GCA for short). These features are intended to replace the existing generic_const_exprs feature which has existed in some form or another since min_const_generics was stabilized back in 2021.
