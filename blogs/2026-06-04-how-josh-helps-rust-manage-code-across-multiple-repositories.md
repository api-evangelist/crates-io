---
title: "How Josh helps Rust manage code across multiple repositories"
url: "https://blog.rust-lang.org/inside-rust/2026/06/04/how-josh-helps-rust-manage-code-across-multiple-repositories/"
date: "2026-06-04"
author: "Jakub Beranek, Ralf Jung"
feed_url: "https://blog.rust-lang.org/inside-rust/feed.xml"
---
The Rust Project maintains several developer tools in separate repositories that must be integrated into the main rust-lang/rust repository for CI distribution and coordinated updates when breaking changes occur. This post explains how Josh, a tool for bidirectional repository synchronization, helps Rust manage code across multiple repositories by enabling workspace subsets and subtree workflows. Josh simplifies the process of keeping external tool repositories in sync with the monorepo while preserving clean commit history.
