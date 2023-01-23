---
published: true
layout: post
title: 'Will I become a Rustacean?'
image: /images/posts/2023-01-23-becoming-rustacean.png
author:
  name: pascal
tags:
- rust
- programming
- Featured
---

I was recently reading [this article](https://medium.com/@SergiAlfonso/why-python-is-not-the-programming-language-of-the-future-193ae73f9e0d) about *"Why Python is not the programming language of the future"*. I'm not sure whether this will happen, but the author makes some very interesting points. One that I'm particularly sensitive about is performance. I grew up as a C/C++ developer (and other languages like Pascal, Assembly, COBOL, Prolog, LISP, or even APL). These were fun times but you had to seriously think about memory management and code efficiency, as we didn't have today's luxury of ridiculously fast processors and gargantuan memory space. 

Since the late 90's though, my world has become dominated by languages such as Java, Python, JavaScript, R, and, while I admit they  have their benefits, I've never felt really comfortable with any of them. They all somehow seem a bit sloppy, too verbose, or cryptic. And they are not truly compiled code, which in my mind means not delivering the highest possible performance. When I went back to school to complete my Master in Computational Science, I recall how much fun it was to use C/C++ again and integrate with high-performance Fortran libraries like BLAS and LAPACK , necessary for quantum physics or astrophysics computations to complete in a 'reasonable' amount of time. 

### Exploring Rust
Anyway, the above article suggests three options to consider for the future: Rust, Go and Julia, and advertises Rust as *"solves the performance issue with the concept of ownership and borrowing"*, which got my attention. Many people also seem to believe that Rust will replace C++, and the January 2023 [TIOBE index](https://www.tiobe.com/tiobe-index/) (ranking programming languages) highlights that *"Performance seemed to be important. C++ competitor Rust entered the top 20 again (being at position #26 one year ago), but this time it seems to be for real."*. So I recently decided to dive into it, and I really like what I see so far.

The Rust framework environment was trivial to [install](https://www.rust-lang.org/tools/install) on my Mac and well supported in Visual Code which is my current IDE. I was basically up and running in a matter of minutes. The language is extremely well [documented](https://www.rust-lang.org/learn) and many [packages](https://crates.io/) (a.k.a. crates) are readily available. 

One interesting thing that Rust has done to me is that, for some reason, I'm actually reading the docs rather than diving right away into writing code like the uncontrolled geek I am. Rust feels like a peaceful space where everything is explained in clear a concise terms, making you want to understand it first. Now of course I do have written a few lines of codes, but in a controlled and well behaved manner (otherwise the Rust compiler will scold you). 

### Rust Packages 

One of my worry was, as a relatively new language, it would not yet be equipped with the libraries I need to support my research and development projects. But this has not been the case so far. For example I quickly found [Diesel](https://diesel.rs/) to connect to databases, and there are several options for buildings APIs like [Warp](https://docs.rs/warp/latest/warp/), [Rocket](https://rocket.rs/), [Actix](https://actix.rs/), or [Reqwest](https://docs.rs/reqwest). 

One crate that got my particular attention is [Unit of measurements](https://docs.rs/uom/latest/uom/). This is a topic of high interest to me as, as a member of the CODATA group focusing on the [Digital Representation of Units of Measurement (DRUM)](https://codata.org/initiatives/task-groups/drum/), it is the the kind of tools we are looking for. Thanks to this package, units can properly be expressed in Rust out of the box based using the [SI standard](https://www.bipm.org/en/measurement-units). The developers also took the correct approach of using *quantities* rather than *units* (which can be ambiguous). Too early for me to tell how well this performs, and I plan to further investigate once I have my Rust skills up to speed. But it tells me that the Rust community is paying attention to standards and the needs of the data, scientific, and research communities. This would be a great option to build APIs around units and quantities of measurements, or fundamental physical constant constants.

### C/C++ vs Rust?
I'm sure there are many differences between C/C++ and Rust, but the one that  I quickly discovered is code safety and robustness. C/C++ will let you do anything you want:  good things, great things, bad things, and very very bad things. Rust on the other hand elegantly forces you to think ahead and be disciplined about your code, making sure potential issues are all caught at compile time, not at runtime, when it's too late. This can at first be unsettling or feel tedious, but you quickly appreciate how valuable it is.

### Becoming Rustacean
"Rustaceans" are people who use Rust, contribute to Rust, or are interested in the development of Rust. You can find them at [https://rustaceans.org](https://rustaceans.org), or meet the community on [Discord](https://discord.gg/rust) or other places like [Zulip](https://rust-lang.zulipchat.com/). It looks like I may have just become one, and I'm looking forward to further explore Rust. Stay tuned.
