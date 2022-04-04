# Operability Reviews

## What is an Operability Review?

**The goal of the Operability Review is to determine the readiness of a system
or product before its launch date.**

An Operability Review is part of a launch process that gives us a chance to
think through important factors and answer critical questions such as, but not
limited to, the following:

* How does the system operate?
* How do we observe its behavior?
* In what ways can the system fail?
* How can we detect failure within the system?
* How do we address failures and confirm the resumption of expected behavior?

The review is an opportunity to broadly communicate the status of a system or
product ahead of its launch, to demonstrate our confidence in its readiness,
and to receive feedback crucial to the success of its launch. An Operability
Review reinforces our shared practices and encourages us to design resilient
solutions.

### Deferred Launch

If it is determined that the system or product being reviewed is not ready
(i.e. it's not observable or its failure scenarios are not defined) the launch
date may be deferred. It is recommended that launch dates not be confirmed
until a successful Operability Review is completed.

## When does it occur?

After an architecture review and generally _no sooner than 1-2 weeks
before launch_.

## Who attends?

Typically those with direct knowledge of the system and those that may consume
it will be in attendance. These people, among others, will include:

* The team or working group who has prepared for the launch
* Key stakeholders who may be supporting elements of this product (i.e.
  customer-facing teams)
* Product/Project/Program managers

## What do we discuss?

A number of topics will be reviewed. For clarity, we can think of these
topics in terms of primary and secondary concerns. Primary concerns are those
that **must have positive answers** before a launch is approved. Secondary
concerns are still important, but may not apply in all situations.

### Primary Concerns

#### Documentation

* Describe, in a sentence, what the system/product is and what problem it
solves/solution it provides.
* Does this launch involve any new infrastructure? 
* Describe how updates are deployed to production.
* Describe how development is done on/for this system/product.
* Provide relevant links to documentation on the system/product such as a
detailed description, diagrams, etc.

#### Normal Operation

* Describe the expected behavior of a well-functioning system or product.
* How is this behavior observed (i.e. system metrics, instrumentation, logs,
etc.).
* Provide relevant links.

#### Failure Scenarios

* Describe failure scenarios we've _experienced_ with this system.
* Describe failure scenarios we've _anticipated_ with this system.
* How will be know if/when we encounter any of the above failure scenarios
(i.e. alarms/alerting, failure metrics)?
* Provide relevant links to documentation (i.e. runbooks) that detail how:
	* Failures will manifest (i.e. customer impact, downstream effects)
	* Failures will be addressed (i.e. via automated and/or manual intervention)
	* Notifications will be managed during a failure.

#### Communication

* Who are the people and teams that need to be aware of this launch?
* Have they been notified?
* Which media/channels are being used to communicate this launch?
* Does the communication include information recipients can use to contact
us in the event of an issue they discover post-launch?
* Where/how do users report bugs/issues/concerns post-launch?

### Secondary Concerns

#### Performance Benchmarks

* Describe how we measure the performance of the system (i.e. speed, throughput,
capacity, etc.)
* Describe the expectations we have for how the system should perform and how
we measure reality versus those expectations.
* Provide relevant links.

#### Crash Tests

* Describe how we've tested the limits of the current system's performance
(i.e. load/stress tests).
* Describe how we've tested the system's behavior during failure (i.e.
GameDay/Chaos events, postmortem reviews).
* Describe any outstanding testing that needs to be completed before launch.

#### Pre-production
* Has any of the system/product been in production for some time already?
* If not, could it have been?
  * If so, why did we choose not to do so?

#### Feature Flags and Ramped Launching

* Do we have any on/off switches for this system/product launch?
* Is it possible to turn up this system/product on a percentage basis or launch
it dark?
  * If so, provide links to relevant documentation.



