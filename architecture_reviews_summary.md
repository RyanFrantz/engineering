# A Summary of Architecture Reviews

I have a number of ideas about how and why
[architecture reviews (ARs)](/architecture_reviews.md) should be conducted; it
seemed useful to provide an overview of that content to introduce those ideas.

## What is an AR?

An AR is a structured conversation among engineering peers about software
designs and operational approaches we use. These discussions surface the impact
on long-term engineering practice within our organization. A goal is to aid the
direction of our collective energies in ways that better support the products
and experiences we deliver to our customers. Another goal is to socialize how we
think about writing software and the building and operation of systems.

ARs focus on outcomes more than specific implementations.

### What is the intent of an AR?

First, they are intended to help clearly define and communicate a technical
problem we need to solve. Is this truly a problem we have? Is this the right
thing to be working on right now?

Second, it is an opportunity to solicit feedback on ideas, to refine them. No
single engineer can contain the entirety of the stack in their mind; drawing on
peers lends additional perspectives that better shape the problem.

Finally, the AR helps surface important decision-making context and identify
trade-offs. Knowing the criteria we use to gauge choices is just as critical as
the choices themselves. We do this by capturing the discussions in a form that
others can consume later. These artifacts are useful for understanding the
evolution of our systems and are a concrete example of our engineering culture.

## What is an AR not?

ARs are not approval mechanisms. For example, an AR cohort may decide that a
given approach is not in our interests (i.e. costs outweight benefits) or the
given problem doesn't need to be addressed at the time. The engineers presenting
the given problem may choose to proceed with the work. They can do so, knowing
the consensus has been documented, at least.
