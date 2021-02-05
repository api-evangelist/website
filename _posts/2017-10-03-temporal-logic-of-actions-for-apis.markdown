---
published: true
layout: post
title: Temporal Logic of Actions For APIs
date: 2017-10-03T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Testing
  - Algorithms
  - Observability
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/status-berlin_dark_dali.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/status-berlin_dark_dali.jpg" align="right" width="40%" style="padding: 15px;" /></p>I'm evolving forward my thoughts on algorithmic [observability](http://apievangelist.com/2017/02/28/a-checklist-for-api-observability/) and [transparency](http://apievangelist.com/2016/08/04/pushing-for-more-algorithmic-transparency-using-apis/) using APIs, and [I was recently introduced to TLA+, or the Temporal Logic of Actions](https://en.wikipedia.org/wiki/TLA%2B). It is the closest I've come to what I'm seeing in my head when I think about how we can provide observability into algorithms through existing external outputs (APIs). As I do with all my work here on API I want to process TLA+ as part of my API research, and see how I can layer it in with what I already know.

TLA+ is a formal specification language developed by Leslie Lamport, which can be used to design, model, document, and verify concurrent systems. It has been described as exhaustively-testable pseudocode which can provide a blueprint for software systems. In the context of design and documentation, TLA+ can be viewed as informal technical specifications. However, since TLA+ specifications are written in a formal language of logic and mathematics it can be used to uncover design flaws before system implementation is underway, and are amenable to model checking for finding all possible system behaviours up to some number of execution steps, and examines them for violations. TLA+ specifications use basic set theory to define safety (bad things won't happen) and temporal logic to define liveness (good things eventually happen).

TLA+ specifications are organized into modules.Although the TLA+ standard is specified in typeset mathematical symbols, existing TLA+ tools use symbol definitions in ASCII, using several terms which require further definition:

- **State** - an assignment of values to variables
- **Behaviour** - a sequence of states
- **Step** - a pair of successive states in a behavior
- **Stuttering Step** - a step during which variables are unchanged
- **Next-State Rlation** - a relation describing how variables can change in any step
- **State Function** - an expression containing variables and constants that is not a next-state relation
- **State Predicate** - a Boolean-valued state function
- **Invariant** - a state predicate true in all reachable states
- **Temporal Formula** - an expression containing statements in temporal logic

TLA+ is concerned with defining the correct system behavior, providing with a set of operators for working through what is going on, as well as working with data structures. There is tooling that has been developed to support TLA+ including an IDE, model checker, and proof system. It is all still substantially over my head, but I get what is going on enough to warrant moving forward, and hopefully absorbing more on the subject. As with most languages and specifications I come across it will just take some playing with, and absorbing the concepts at play, before things will come into focus.

I'm going to pick up some of my previous work around [behavior driven assertions](http://apievangelist.com/2016/10/06/adding-behaviordriven-development-assertions-to-my-api-research/), and how [assertions can be though of in terms of the business contracts APIs put forward](http://apievangelist.com/2016/04/08/the-api-assertions-we-make-believe-in-and-require-for-our-business-contracts/), and see where TLA+ fits in. It's all still fuzzy, but API assertions and TLA+ feels like where I want to go with this. I'm thinking about how we can wrap algorithms in APIs, write assertions for them, and validate across the entire surface area of an algorithm, or stack of API exposed algorithms using TLA+. Maybe I'm barking up the wrong tree, but if nothing else it will get me thinking more about this side of my API research, which will push forward my thoughts on algorithmic transparency, and audit-able observability.
