---
title: "Rustup update: our plans for the 1.30 release cycle"
url: "https://blog.rust-lang.org/inside-rust/2026/07/03/rustup-update-1.30/"
date: "2026-07-03"
author: "rami3l"
feed_url: "https://blog.rust-lang.org/inside-rust/feed.xml"
---
This blog post is t-rustup 's first attempt of providing a more transparent view of the team's current work. Here, we summarize the focus areas of t-rustup in the ongoing release cycle leading to the future 1.30.0 release, hoping to inform you of our future plans, and ask for your feedback to help us make rustup better. Ongoing Changes Refining the implicit installation behavior In rustup 1.27 or earlier, rustup would implicitly install the active toolchain once found missing whenever rustup is invoked, including proxy invocations such as rustc and cargo .
