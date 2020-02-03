---
layout: post
title: "Why we need trunk based development practices"
date: "2020-02-02 10:41:21 +1100"
---

** Trunk Based Development **

Trunk Based Development (TBD) is that thing that everyone wants to do - you know - if it weren't for all the downsides that come with it..
I'm going to challenge those perceived problems in this post because I think TDB and its supporting practices are oftentimes shot down by well meaning engineers and managers.

So let's explore what these set of practices are and the value they can provide.

** Not Just About TDB **

Firstly, it's worth understanding it isn't just about Trunk Based Development. I'm excited for the set of TDB practices because it's not _just_ about implementing a single, narrow, workflow in isolation; It's also about all the supporting practices around TDB. Together, they enable each other and create a system and workflow greater that just the sum of their parts.

But what are they? Let me list a few.

Some supporting practices:
- Feature Toggles
- Test Driven Development
- Observability
- Lean Software Development
- Decoupling Deployments from Releases

** As A Whole **

The interesting thing about the list above is it is not definitive in any sense. These are simply some well known practices that encourage and carry forward small units of work.
When put together, these practices make up a system that has small units of work from beginneing to end.

** Small Units **

Why is this even good? A simple analogy may suffice. Think of a tetris game, it get's harder as we are given more difficult pieces and as the speed of these pieces falls faster and faster. There are square blocks, lines, corners, s-shapes.. What if we could simply break down these pieces in to their single unit square blocks. Tetris would be a simpler game indeed.

*** Feature Toggles ***

This practice is much bigger than I initially thought. It's a very different way of programming. Small changes are relatively simple, refactoring is different though.

*** Test Driven Development ***

Comprehensive test suites



** Removing Hurdles, Blockers and Rings Of Fire **

We can think of this as much about enabling developers adding value as removing the blockers.


** Problems **

- Product Owners usually sign off on a feature, bug fix or change going in to the system. One thing I've seen is the development team being held up from deploying/releasing (same thing) in to their staging environment because the PO doesn't want the risk of more than 1 change going in at once.
- Deployments have to be stopped, because a deploy means a new release. And for whatever reason, we are not yet ready to release something. Maybe there is a bug, it's an important time for the system or there are users, QA team or PO's doing some testing.
- Giant merges and conflicts still happen.
-





