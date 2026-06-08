---
title: C++20 coroutines framework for embedded applications (STM32, nRF52840)
subtitle:
tags: ["C++", "C++20", "Coroutines", "Embedded", "MCU", "STM32", "nRF52840"]
date: 2026-04-26
---

{{< github-repo name="vagran/pulse" >}}

One day, I realized that I still couldn't use C++20 coroutines in my embedded projects targeting
STM32 and nRF52840 microcontrollers. While Rust developers can take advantage of coroutines through
the Embassy framework, there was no comparable solution available for C++, despite coroutines having
been part of the language for years.

So I decided to build one myself.

<!--more-->

The result is an embedded coroutine framework that I'm quite happy with. One feature I'm especially
proud of is its memory allocator. It is unique enough that I may eventually move it into a separate
project. The allocator allows you to balance maximum allocation size against per-block overhead
through compile-time configuration. In its most compact configuration, the overhead can be as low as
two bytes per allocated block, making it suitable even for the smallest microcontrollers.

I've also created a detailed tutorial that walks through the framework and its design:

{{< github-repo name="vagran/pulse-tutorial" >}}
