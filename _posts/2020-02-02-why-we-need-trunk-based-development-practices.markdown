---
layout: post
title: "Why we need trunk based development practices"
date: "2020-02-02 10:41:21 +1100"
---

# Trunk Based Development

Trunk Based Development (TBD) is that thing that everyone wants to do - you
know - if it weren't for all the downsides that come with it.. It sounds great
at first because you can simply merge or commit straight to your master branch
and that's it, that new feature or code is going to production immediately. But
nothing is this simple and there are real problems encountered when adopting
this in isolation.

I'm going to challenge those problems in a series of posts because I think TDB
and its supporting practices are oftentimes shot down by well meaning engineers
and managers too early on in the adoption process.

Later, I'll contrast Trunk Based Development with longer lived release branching
and offer some thoughts and opinions.

For now let's jump in and explore what these set of practices are and the value
they can provide.

# Not Just About TDB

Firstly, it's worth noting that it isn't just about Trunk Based Development as a
single isolated practice.

True value is found when using the entire set of TDB practices, as a whole. Not
about implementing a single, narrow workflow in isolation.

These set of practices support each other and enable a workflow greater that
just the sum of their parts. They facilitate a system designed so that engineers
can deploy small units of work.

What are these supporting practices?

A few are:

- Feature Toggles
- Test Driven Development
- Observability
- Lean Software Development
- Decoupling Deployments from Releases

# As A Whole

The list above is not definitive in any sense. These are simply some well known
practices that encourage and carry forward small units of work. When put
together, these practices make up a system that has small units of work from
beginning to end.

If there were a process in the middle of all of this that accumulated work in to
one big chunk then the downstream processes would lose a lot of their value.
They would be slowed considerably.

> When put together, these practices make up a system that has small units of
> work from beginning to end.

# Small Units

Why are small units good?

The short answer is _they are easy to work with._

Once big chunks of work are broken down in to small units, we can reason about
them more easily. If there is a problem with work on that unit, it is easy to
understand and overcome. Feedback comes back faster, and this enables quicker
iteration over the development, or the problem.

An analogy might help. Let's think of a tetris game. It get's harder as more
difficult pieces fall and as the speed of these pieces fall faster and faster.
There are square blocks, lines, corners, s-shapes.. but what if we could simply
break down these pieces in to their single unit square blocks?
Tetris would be a simpler game indeed. The system is geared toward deployment.

![tetris](https://{{ site.url }}/assets/posts/1_tetris.jpeg)

We can identify some overhead here. We still need to break up these big units of
work in to smaller units. This process is valueable in itself and we realise
this value to its potential when we start to decompose larger units in to
smaller ones as early as possible. We can then plan and understand how and when
we are going to deal with the smaller units with more foresight.

# More to come

This concludes the first post of this series, more will come which look at
practices that enable trunk based development and how we might use them.
