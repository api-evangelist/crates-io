---
title: "Rustup 1.29.1 beta: call for testing!"
url: "https://blog.rust-lang.org/inside-rust/2026/07/14/rustup-1.29.1-beta-cft/"
date: "2026-07-14"
author: "rami3l"
feed_url: "https://blog.rust-lang.org/inside-rust/feed.xml"
---
We are excited to announce that rustup 1.29.1 beta is now available for testing and we are currently looking for testers. What's new The headlines of this release are: Concurrency in certain rustup operations has been improved: When running rustup update , rustup will first check for possible updates in parallel. pr#4752 When running rustup component add with multiple components, they will be installed concurrently.
