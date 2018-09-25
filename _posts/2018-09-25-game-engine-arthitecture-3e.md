---
layout: post
title: "Game Engine Architecture, 3rd Edition"
date: 2018-09-25 18:06 +0800
categories:
  - Notes
  - Book
tags: game game-engine
comments: true
---

This is a note of *Game Engine Architecture*, 3rd Edition written by Jason Gregory.

{% include toc %}

## Part 1. Foundation
### Chapter 1. Introduction

What is game?

- 1979: toy
- Today (2018): multi-billion-dollar mainstream industry

> In this book you will learn:
> 
> - how real industrial-strength production game engines are architected;
> - how game development teams are organized and work in the real world;
> - which major subsystems and design patterns appear again and again in virtually every game engine;
> - the typical requirements for each major subsystem;
> - which subsystems are genre- or game-agnostic, and which ones are typically designed explicitly for a specific genre or game; and
> - where the engine normally ends and the game begins.

## Chapter 2. Tool of the Trade

### 2.2 Compilers, Linkers and IDEs

The machine code in an object file is:

- *relocatable*, meaning that the memory addresses at which the code resides have not yet been determined, and
- *unlinked*, meaning that any external references to functions and global data have not yet been resolved.

Some useful compiling tags:

```
$clang --std=c++14 foo.cpp -o foo.o --Wall -O0 -g
```

where `--Wall` turns on all warnings, `-O0` turns off all optimizations, and `-g` generates debugging information. In Windows, the similar command line is like that:

```
cl /c foo.cpp /Fo foo.obj /Wall /Od /Zi
```