---
authors:
- flavorjones
categories:
- Agile
- Humans
date: 2015-11-02T08:45:40-05:00
draft: true
short: |
  Our brains are naturally limited. This can be a curse, or it can be a gift, depending on how you look at it.
title: Abstraction, or, The Gift of Our Weak Brains
---

## Tale of a Prodigy

There's a famous story about [John von Neumann][] and the ["Two Trains Puzzle"][2trains].

This particular puzzle is a math problem, involving two trains travelling towards each other, and a fly that's whizzing back and forth between their windshields: How far does the fly travel before it gets squashed?

The hard way to solve this problem is to [generate an infinite series][2trains] representing the fly's path, and to compute its sum. Most humans aren't capable of doing this calculation in their head.

But there's a shortcut to the solution, which becomes obvious once you realize that

1. you know the __total time__ the fly is traveling (based on the trains' relative speeds);
2. and you're given the __fly's speed__.

A simple velocity calculation later, and you have the answer.

According to <u>[The Legend of von Neumann][]</u>, here's what happened when the puzzle was posed to Von Neumann:

> ... he solved it in an instant, and thereby disappointed the
> questioner: "Oh, you must have heard the trick before!" "What
> trick?" asked von Neumann, "All I did was sum the geometric series."

Von Neumann was a remarkable math prodigy who was famous for his [extraordinary cognitive abilities](https://en.wikipedia.org/wiki/John_von_Neumann#Cognitive_abilities), so perhaps it's unsurprising that he was able to compute an infinite series so quickly.

If you're paying attention, though, it should be very surprising that such an extraordinary intellect didn't see and use the shortcut to solve the problem.

__Why didn't Von Neumann see and use the shortcut?__ Was it easier for him to do the calculation than to search for an unnecessary (to him) abstraction?

  [John von Neumann]: https://en.wikipedia.org/wiki/John_von_Neumann
  [2trains]: http://mathworld.wolfram.com/TwoTrainsPuzzle.html
  [The Legend of von Neumann]: https://www.jstor.org/stable/2319080


## A Tale of a Non-Prodigy

When I was studying physics in college, I felt pretty dumb for a long time. For the first time in my life, I was surrounded by people who were smarter than I was, and who were able to grok complex systems and perform elaborate calculations more quickly than I could.

I'm pretty sure everyone else thought I was dumb, too. I needed study partners, and lots of topics I just ... didn't ... get. I struggled hard to try to understand [Classical Mechanics][cm], [E&M][em], and [Quantum Mechanics][qm]. I almost failed [Diff EQ][de].

This was a huge source of pain and stress for me. I had never failed at anything before. And so I struggled, _hard_, to find a better way to learn these concepts and internalize their lessons. I spent a lot of time and effort trying (and discarding) various paradigms to intuitively explain complex systems.

Eventually, I hit a tipping point. Once I modeled the abstractions appropriately in my mind, I was able to reason about complex behavior as well or better than my peers. I suddenly started getting flashes of insight, and was able to leverage previous abstractions when solving take-home problems.

This felt like a bit of a superpower. It felt like I had finally modeled the problem properly in my brain, and as a result was able to ignore extraneous details and solve the Big Picture problems.

Much later in life, I would read Hofstadter's <u>[Gödel, Escher, Bach][geb]</u> and realize I had metaprogrammed my brain for a particular domain, and it had allowed me to use abstractions as a first-class language for learning and reasoning.

Why did I do this, when some people with higher IQs were perfectly capable of it, but didn't appear to be doing it? __Was it because the lack of abstractions was more painful for me than for them?__

  [em]: https://en.wikipedia.org/wiki/Electromagnetism
  [cm]: https://en.wikipedia.org/wiki/Classical_mechanics
  [qm]: https://en.wikipedia.org/wiki/Quantum_mechanics
  [de]: https://en.wikipedia.org/wiki/Differential_equation
  [geb]: http://www.amazon.com/G%C3%B6del-Escher-Bach-Eternal-Golden/dp/0465026567


## The History of Science is a History of Abstractions

Recently, [Brian Skinner][] wrote an [amazing post][ribbonfarm] about how many of our scientific observations are a direct result of humans seeking to find intuitive abstractions to explain complex phenomena:

> As an extreme example, consider that human thinking struggles to
> describe even individual atoms with real precision. How is it, then,
> that we can possibly have good science about things that are made up
> of many atoms, like magnets or tornadoes or eukaryotic cells or
> planets or animals? It seems like a miracle that the natural world
> can contain patterns and objects that lie within our understanding,
> because the individual constituents of those objects are usually far
> too complex for us to parse.

The discussion there is about how humans _choose to reason_ about electrons in an electric circuit, versus how electrons _actually_ behave.

The key point being that electron behavior is actually so complicated, involving complex interactions between quantum probabilities, electromagnetic repulsion, and electric fields, that human brains are piteously underpowered to calculate what's going on.

The net result, though, is that we model the __aggregate__ behavior of all the electrons in the circuit, versus modelling __each and every__ electron. And that statistical model works amazingly well in a wide variety of circumstances.

Imagine an alien race with the cognitive faculties to calculate individual electron trajectories. Would those aliens fall back to the same abstraction? Or would they simply continue, as Von Neumann did, do do the calculations the hard way?

  [Brian Skinner]: http://www.ribbonfarm.com/author/brian/
  [ribbonfarm]: http://www.ribbonfarm.com/2015/10/29/quasiparticles-and-the-miracle-of-emergence/

## NASA's Voyager: Legacy Code Like You've Never Seen

Recently, NASA put a call out for FORTRAN developers to [continue work on the Voyager spacecraft software][vger]. Everyone on the original team has retired from NASA at this point, meaning that the code running Voyager is literally two human generations old.

What kind of problems do you think exist around such extreme legacy code? In an [interview with Popular Mechanics][popmech], the program manager for the Voyager program said:

> ... it's time to turn back to old documents to figure out the logic
> behind some of the engineering decisions. Dodd says it's easy to
> find the engineering decisions, but harder to find the
> reasoning. This means combing through secondary documents and
> correspondence hoping to find the solution, trying to get in another
> engineer's head.

Holy cow.

I mean, I realize that the solution had severe constraints placed on it (miniscule processing power, and 64KB of RAM). But the situation being described sounds more serious than that.

> _"trying to get in another engineer's head."_

Think about that for a moment. Not "trying to understand the code", not "trying to understand the implementation", but __"trying to understand how the author was reasoning about the universe at the time."__

Wouldn't it have been easier if the relevant abstractions had been captured when that code was written?

  [vger]: http://www.theregister.co.uk/2015/10/31/brush_up_on_your_fortran/
  [popmech]: http://www.popularmechanics.com/space/a17991/voyager-1-voyager-2-retiring-engineer/


## The Impact of Ability on Developing Abstraction

The repeating theme of these stories is: People seem to resort to developing the proper abstraction only when they hit the limit of their computational power.

* John von Neumann didn't bother to look for a more elegant solution, because he was able to brute force an infinite series so easily.
* I needed to develop useful abstractions in college, to compensate for my brain's relative lack of compute power.
* When humankind hits physiological limits of what a brain is capable of, science seeks and finds appropriate abstractions that allow civilization to advance.
* And NASA computer scientists, perhaps some of the smartest people assembled since the Manhattan Project, end up writing code that is so inscrutable that modern-day maintainers are forced to read the authors' mail to figure out what the hell the software was intended to do.

I can only hold one or two things in mind at a time. Maybe three, tops. I want to think deeply about a thing until I'm done, and then move on. Ask anyone who's tried to have a conversation with me when I have two or three things already in my head -- I tend to be a total basket case at these times.

Some people appear to be able to hold much more state in their brain than I can. It's the only way I can explain spaghetti code with light test coverage. When I ask myself, "How can anyone understand this?", the answer is usually, "Because the author must have more prodigious computing power in their brain than I do."

And that's OK. Except for when you have to deal with other people. Which is probably most of the time.

Whoops.


## Complexity Without Empathy Considered Harmful

Not every smart person I know suffers from a reluctance to find and exploit appropriate abstractions. Most of the people I know who strive for the right abstraction share a common value: __empathy__. They all have empathy for their current teammates and future developers.

This empathy for fellow developers can emerge in a number of ways. Perhaps the best known manifestation is Knuth's ["Literate Programming"][lp]:

> Let us change our traditional attitude to the construction of
> programs: Instead of imagining that our main task is to instruct a
> computer what to do, let us concentrate rather on explaining to
> human beings what we want a computer to do.

Another great example is Eric Evans's ["Domain Driven Design"][ddd] (as explained in his [book of the same name][dddbook])

> A domain model ... is not just the knowledge in a domain expert's
> head; it is a rigorously organized and selective abstraction of that
> knowledge. ... The model is the backbone of a language used by all
> team members.

At Pivotal, empathy takes form in our engineering practices.

__We test-drive__, which forces us to think deeply about the proper abstractions in the code as we're writing it.

__We pair program__, which forces us to explain, before the code gets committed, the reasoning and intentions behind the code.

__We rotate frequently between teams__, meaning that we're almost always teaching someone a new domain and codebase, and so we are incentivized to make sure the code is understandable and abstracted correctly; and we feel acute pain around explaining poorly abstracted code.


  [lp]: http://www.literateprogramming.com/knuthweb.pdf
  [ddd]: https://en.wikipedia.org/wiki/Domain-driven_design
  [dddbook]: http://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215
