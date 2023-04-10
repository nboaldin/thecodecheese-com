---
title: "Rust Ownership Made Simple"
date: 2022-07-01T21:20:50-05:00
draft: true
author: "The Code Cheese"
authorLink: "https://twitter.com/thecodecheese"
categories:
- programming
- rust
tags:
- pointers
- references
- ownership
---

## Rust Ownership Made Simple

I cannot take credit for what I am about to write. All I can say, is that when someone presented to me 3 simple rules of how ownership works in Rust, I feel like I finally kinda understood it. These following rules were presented to me by Lyubomir Gavadinov in his Udemy course [Learn Rust by Building Real Applications](https://www.udemy.com/course/rust-fundamentals/). He also explains Stack and Heap memory in a very concise way in this course. Do yourself a favor and pick it up if you want an intro to the Rust language.

Ok, on to the Rust ownership rules.

### 1. Every value is owned by a variable

This may seem obvious, but it's really not. I will try to explain. In a lot of other programming languages 

```rust
func main() {
  println!("Code to the Cheese")



}

func cheese_me() -> {

  // String is really a vector of u8
  let mut cheese = String::new();

}
```

### 2. When the owner moves out of scope, the value will be removed from memory

### 3. There can only be one owner at a time


