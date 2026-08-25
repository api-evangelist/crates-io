---
title: "Experiment in reducing target directory size on nightly"
url: "https://blog.rust-lang.org/inside-rust/2026/08/18/reducing-target-dir-size-on-nightly/"
date: "2026-08-18"
author: "Jakub Beránek"
feed_url: "https://blog.rust-lang.org/inside-rust/feed.xml"
---
TL;DR: The Cargo Team will be rolling out an experiment to identify user impact for a proposed change. Cargo will enable the -Zembed-metadata=no feature on the nightly channel by default, which can help reduce the size of the target directory somewhat. This is an experiment designed to gather feedback about viability of this feature.
