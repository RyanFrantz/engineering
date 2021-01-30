# Architecture Reviews

["Engineers cause change... We immediately run into three practical difficulties
when we consider the engineer's change: the engineer doesn't know where [they are]
going, how [they are] going to get there or if anyone will care when [they
do]".](https://files.eric.ed.gov/fulltext/ED276572.pdf)

["Technology choices don't happen in isolation. They have a scope that touches
your entire team, organization, and the system that emerges from the sum total
of your choices".](http://mcfunley.com/choose-boring-technology)

We perform architecture reviews to surface potential changes to, to solicit
feedback on, to develop confidence in, and gain consensus on, new software
designs or operational approaches (departures) even (especially) if we are
uncertain what the final outcomes will be. These discussions are made up of
peers, stakeholders, and anyone who is curious. All attendees are expected to
be open-minded, fair, and even-handed. Participation is intended to be broad.

## Do I Need an Architecture Review?

If your first inclination is to begin building something, it's very likely
you've not thought through the problem you need to solve. Think deeply about the
work and seek first to use existing technology/patterns. If you do not find an
existing solution that meets your needs, it may still be out there. Reach out
to fellow engineers and solicit feedback. Only afterwards, if you still believe
you must depart from current solutions or approaches, initiate an architecture
review.

## How does One Prepare for an Architecture Review?

First, describe the problem that is being addressed. If the work is intended to
replace an existing solution, describe what is currently in place and why it is
believed that a change is necessary.

Provide relevant content from documentation, engineer anecdotes, diagrams or
other visual aids, etc. An RFC or design document is an excellent place to
consolidate this content. Generally, a design document should include some, or
all, of the following elements:

* A description of the problem we are looking to solve.
* What we currently use that we believe will not address our problem.
  * An explanation of why we believe existing solutions will no longer suffice.
* Benefits and potential costs (time, money, opportunity) of the proposed design.
  * How does the proposal better solve this problem?
  * What are the known downsides to implementing this change?
* Initial questions collected from peers and/or the Architecture Review Working
  Group. [1]

*It is not required, though strongly recommended, that the proposal be reviewed
by the Architecture Review Working Group to help refine it ahead of a scheduled
architecture review where a broader audience is expected to attend.*

### Proofs-of-Concept

It is always informative to spin up some VMs/containers and write a few lines of
code to ascertain the rough edges of a solution. By all means, do so. Be
cautious, however, that you do not pursue a proof-of-concept too deeply before
performing an architectural review; your time is valuable and is likely to bear
more fruit spent in a review.

## How is an Architecture Review Performed? 

An Architecture Review (AR) is a dialogue where an idea is put forward and
reviewed. It is not a presentation to persuade or a sales pitch; such events
tend to be one-sided and presuppose a decison has been made. Rather, the
anticipated benefits and costs associated with the departure are discussed.
Most important to this process is attempting to reduce ambiguity so that the
operation of our systems may be easier to reason about. We can never eliminate
complexity but when we appreciate that ["[c]omplex systems are intrinsically
hazardous systems"](http://web.mit.edu/2.75/resources/random/How%20Complex%20Systems%20Fail.pdf)
we will come to see ARs as a means of defense against future failure. To that
end, during a review, questions like the following should be raised:

* What is the purpose of this proposal? Why do we believe we should do this?
* What is the current architecture? How does this proposal diverge from it? 
* Have we discussed trade-offs (using existing systems already in place versus
  this proposal)? 
* Do we understand the costs of this architecture?
  * What are the known trade-offs? What were the criteria for making choices?
  * Is there additional work that may be required (i.e. migrations) as a result
    of doing this work?
* Do we understand what the long term maintenance of this architecture will be? 
* Will this prohibit us from doing something else in the future? 
* Are we impacting visibility, measurability, debugging or any other operability
  concerns? (think internally and for other teams)
* Are we impacting testability, security, performance or any other product
  quality concerns? (think internally and for other teams)

In general, the AR is not intended as an approval mechanism. This does not mean
that participants cannot have dissenting views. The expectation should be that
everyone involved has the right to voice their views in a professional and
supportive manner. For example, if someone identifies an issue with a proposal,
the discussion does not end at the point of its discovery; rather, a
conversation should help everyone come to a shared understanding of the
shortcoming and provide recommendations for addressing it.

Some discussions may result in an agreement that no work will proceed (i.e. a
better solution already exists or the problem no longer needs to be solved) but
by and large, ["[e]ngineers (both presenting and participating as audience)
need to understand the purpose of the architecture review is to develop better
outcomes."](https://www.kitchensoap.com/2017/08/12/multiple-perspectives-on-technical-problems-and-solutions/)

## Who is in Attendance?

Typically those with direct knowledge of the system and those that may consume
it will be in attendance. These people, among others, will include:

* Team/working group presenting this change
* Key stakeholders (Managers, TLs, and/or an Architecture Review Working Group)
* Anyone who wants to learn more about the existing architecture or proposed
  change

## What is the Outcome of a Review?

While an AR should not be viewed as an approval mechanism, it is expected that
the process is managed by a trusted cohort of engineers whose combined
experience and influence can be used to effectively drive the direction and
execution of work. To aid in the decision-making process and to provide a means
for transparently communicating the process, each AR should output the following:

* A set of written meeting minutes that captures:
  * The review itself including all questions, their answers, and any references
    for follow-up.
      * Any unresolved questions should be indicated as such.
  * An agreement on the expectations for this proposal.
    * Do we need to solve this problem?
    * Is the problem sufficiently solved with an existing solution we can reuse?
    * Does the proposal need additional information or data?
    * If we agree that the departure is warranted, is there consensus on the new
      approach?

## Footnotes

[1] An Architecture Review Working Group is a cohort of engineers that bring a
    range of experience and perspectives to these discussions and are willing
    to put in the time and energy to make architecture reviews successful.
