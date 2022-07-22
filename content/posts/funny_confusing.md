---
title: "Funny, Confusing Rust Values and References"
date: 2022-07-22T11:35:19-05:00
draft: false
author: "The Code Cheese"
authorLink: "https://twitter.com/thecodecheese"
---

## Values and References... huh?

I found a random line on the inter-webs that explained references and pointers. I do not remember where it came from, so if you are the originator, please forgive. It goes like this:

>In rust you can have a mutable value, an immutable value, a mutable reference to an immutable value or a mutable reference to a mutable value.

This is confusing at first glance. Well it's especially confusing if you don't know anything about programming... Why would you be here reading this anyway? Leave. No stay. Anyway, my friend James had some great thoughts on this statement:

>Very confusing, but really all they are saying is that references are pointers behind the scenes. Those pointers can be mutable or not. Whether its value (an address) could point to different memory.
>The memory location/variable it points to, has it's own mutability.
>Though it's a bit different with how rust uses them, due to the added borrow checker. Unlike raw pointers, this introduces "move semantics", where conceptually you consider access to that data - its ownership, to be moved.
>Rust basically guarantees that all of your variables are protected by free, compile-time RWMutexes.
> - At any given time, you can have either one mutable reference or any number of immutable references.

>This also is why you hear of fearless concurrency with rust. It's very difficult to make a race condition or memory access issue in rust.
>With the added bonus that there are no nulls:
> - References must always be valid.

That is enough to chew on for now.
