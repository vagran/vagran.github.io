---
title: Pulse C++ coroutines framework for embedded applications
subtitle:
tags: ["C++", "C++20", "Coroutines", "Embedded", "MCU", "STM32"]
date: 2026-04-26
---

{{< github-repo name="vagran/pulse" >}}

One day I found that I still cannot use C++20 coroutines in my embedded project (targeted to STM32
MCU). You can do it in Rust using Embassy framework, but no same possibility for C++, despite that
C++ coroutines already exist for a long time. So there wasn't other way than writing one.

<!--more-->

I have written one. Also proud of its memory allocator - probably will need to move it to a separate
project since it is pretty unique - you can balance between maximal allocation size and block
allocation overhead by changing compile-time configuration. In its most compact variant it can have
as low as two bytes overhead per allocated block, so it can be used in the tiniest MCUs.

I also have created quite detailed tutorial for the framework:

{{< github-repo name="vagran/pulse-tutorial" >}}
