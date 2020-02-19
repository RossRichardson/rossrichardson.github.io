---
layout: post
title: "Why we need trunk based development practices"
date: "2020-02-02 10:41:21 +1100"
---

# Trunk Based Development

Trunk Based Development (TBD) is that thing that everyone wants to do - you 
know - if it weren't for all the downsides that come with it.. It sounds great
at first because you can simply merge to master and that's it, but there are
real problems encountered when adopting this in isolation.

I'm going to challenge those problems in this post because I think TDB and its 
supporting practices are oftentimes shot down by well meaning engineers and 
managers too early on in the adoption process.

So let's explore what these set of practices are and the value they can provide.

# Not Just About TDB

Firstly, it's worth noting that it isn't just about Trunk Based Development. 

Excitingly, it's about the entire set of TDB practices, as a whole, not only 
about implementing a single, narrow workflow in isolation; It's also about all 
the supporting practices around TDB. Together, these practices enable a workflow
greater that just the sum of their parts. They facilitate a unified system 
designed and ready so that engineers can deploy small units of work.

But what are these supporting practices?

A few are:
- Feature Toggles
- Test Driven Development
- Observability
- Lean Software Development
- Decoupling Deployments from Releases

# As A Whole

The list above is it is not definitive in any sense. These are simply some well 
known practices that encourage and carry forward small units of work. When put 
together, these practices make up a system that has small units of work from 
beginning to end.

> When put together, these practices make up a system that has small units of 
work from beginning to end.

# Small Units

Why are small units good? 

The quick answer is *they are easy to work with.*

Once big chunks of work are broken down in to small units, we can reason about
them more easily. If there is a problem with work on that unit, it is easy to
understand and overcome. Feedback comes back faster, and this enables quicker
iteration over the development, or the problem.

An analogy might help. Let's think of a tetris game. It get's harder as more 
difficult pieces fall and as the speed of these pieces fall faster and faster. 
There are square blocks, lines, corners, s-shapes.. but what if we could simply 
break down these pieces in to their single unit square blocks?
Tetris would be a simpler game indeed. The system is geared toward deployment.

# Feature Toggles

This practice is much bigger than I initially thought. It's also a very 
different way of programming for some people. Small changes are usually straight
forward but larger refactoring efforts can be tricky at first, until some of the
enabling practices are learnt.

Small changes are straight forward in that they can be simple `switch` 
statements or `if{} else{}` blocks to control flow.

```
if config.feature_new_image_processor {
	// new processor code
} else {
	// original processor code
}
```

Larger refactors may involve more substantial work but we can extend the same
pattern. For instance, refactoring a class or series of classes may involve
creating a new class altogether, or a new package, but using these new or old
classes are still controlled through something like an if/else block.

1. Create new DatabaseManager class to replace the old too-long-to-name class.
2. Find the entry point(s) and surround with a control for the feature toggle.

```
if config.feature_big_database_layer_refactor {
	// fancy new db layer
	db = new DatabaseManager()
} else {
	// all the old stuff
	db = new FactoryInternalDatabaseInternalLayerForLolCats()
}

db.connect()
```

Tip 1:
Use an interface to provide a behavioural abstraction layer. This will ensure
that the new class provides all expected behaviours that the program has come to
rely upon.

Tip 2.
An interface is just a beginning. The new class may need to expose some
behaviours and have no need for others. i.e. the new DatabaseManager class
doesn't need to connect() because it does a special light-weight connection call
for each query. It that case, the new class still has a connect() method but
perhaps it is empty.

Tip 3:
Instrument this. Logs, metrics, events.. The feedback loop is important.
When a feature toggle is active or inactive, used or not used, it should be 
recorded and query-able. Other metrics can be added too. It's useful, when
putting in a new feature, to understand how much time it takes too. Don't stop
there, think about what else is important or might be important if it breaks.


## removing toggles

Feature toggles are temporary, they live just as long as they need to until the
new feature proves it is better, or worse. Then it is removed. Feature toggles 
should not outlive their usefulness!

Once feature toggles outlive their usefullness they become technical debt.
Perhaps a little nicer because they are actually quarantined within logical
blocks. Hmmm. That's nice to think technical debt can be somewhat quarantined.
Really, the whole principle of feature toggling is about quarantining areas of
code off from one another.

## the framework

How many feature toggles can be expected within a code base? And how is it all
managed? How far can this idea be taken?

Certainly, it can become a framework of sorts.

## observability

# Test Driven Development

Comprehensive test suites



# Removing Hurdles, Blockers and Rings Of Fire

We can think of this as much about enabling developers adding value as removing the blockers.


# Problems

- Product Owners usually sign off on a feature, bug fix or change going in to the system. One thing I've seen is the development team being held up from deploying/releasing (same thing) in to their staging environment because the PO doesn't want the risk of more than 1 change going in at once.
- Deployments have to be stopped, because a deploy means a new release. And for whatever reason, we are not yet ready to release something. Maybe there is a bug, it's an important time for the system or there are users, QA team or PO's doing some testing.
- Giant merges and conflicts still happen.






