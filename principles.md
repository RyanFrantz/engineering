# Engineering Principles

These are principles I've come to understand and embrace throughout my career.
They are ideals I aspire to when I design, build, and manage systems. There are
certainly edge cases where they may not always apply but, for the most part,
I believe these hold.

This set is by no means exhaustive and subject to change as we learn new things
or think deeper on issues. It is, however, intended to be relatively short in
the hope that it will be easier to remember and internalize.

1. We write software for, and with, other people.
    1. Engineering is a social endeavor.
    2. Technology is simply a means to an end. Define/understand the expected value
       of a thing before building it.
    3. All other principles flow from this.
2. We are always learning.
    1. Despite our best efforts, failure is inevitable. Success requires diligence
       and hard work. In both cases we make a point to study the outcomes and the
       actions that contribute to them.
3. Systems are emergent.
    1. We cannot predict how our systems will be used, how they will grow, or how
       their behaviors may change.
    2. For the properties we know we build in support for observability and
       introspection to ask the system questions.
    3. For everything else, we try to get comfortable with the reality that we
       cannot predict the future and adapt as changes present themselves.
4. Favor simplicity.
    1. As much as possible, design components as simply as possible. This supports
       composability for the problems we need to solve now and those we may
       encounter in the future.
    2. Avoid interleaving concerns even if it appears to be efficient now.
    3. Simplicity may mean more of something, rather than less.
5. Decision-making is as critical as the end result.
    1. Chosen languages, architectures, design patterns, vendors, and more are
       chosen for various reasons and applied for specific purposes.
    2. Leave yourself and others breadcrumbs that provide useful context on the
       what, why, how, and when of those decisions.
      1. Write design documents, RFCs, and conduct recorded (written, at least)
         architecture reviews. Write useful code comments. All of these are
         accessibility features.
         1. Think of this activity as bringing others along with you. These artifacts
            are useful signposts for your peers.
      2. Be explicit; call out the trade-offs that have been made to add clarity
         to the direction and intent of the work.
6. All software has costs.
    1. Costs come in many forms including money, time (to learn, implement),
       operational requirements.
    2. These costs must be understood (at least called out) to help determine
       which are worth paying to deliver value.
7. We design for failure.
    1. We believe we can build solutions that work but we strive to design them
       at least for the failure cases we can anticipate.
8. Software is malleable and ephemeral; product is not.
    1. Availability and reliable functionality of features and APIs must persist.
       How that is delivered is free to change.
    2. Proofs-of-concept are highly flammable.
        1. Be willing to burn them down and start again.
        2. On the other hand, they can unexpectedly light up and take off.
