---
layout: default
title:  "The Polite Code Reviewer"
date:   2017-03-20 17:50:00
categories:
  - en
  - working-with-others
---

## The Polite Code Reviewer

From time to time someone says me
that my code reviews are a little bit "different".
Being the very self-confident person that I am,
I started to ask myself (and other people)
which could I do to make them better.
For my huge surprise,
the "difference" at that time was a very good thing.
So I'll try to break down into steps
the though process that make me review code
the way I do nowadays.

### TL;DR

 - Code Review is an incredible opportunity to educate but,
in many cases,
it's even more important as a learning experience.
 - Don't comment before understanding the reasoning behind the changes.
 - Spend the same energy recognizing good stuff
(encourage and/or praise it)
that you apply to find bad stuff.
 - Write your thougts about the changes
as they were be referred in the future (they probably will).
 - Point clearly and with (code) counter examples
everything that is not that good.
 - Recognize the effort that the coleagues employed
on try to make the best they can.

### Read the code (_and not "just" the diff_ )

At least for me
is very tempting to just glance my eyes over the _diff_.
And I normally try my best to avoid this urge
and *really*® read the changes and
understand the motivations
before make up any type of conclusions.

#### The objective here is to bring up the motivations

 - Why something is writen in the way it is?
 - What was the thought process?
 - Can I learn something from it?
  (not just technically but even about the business?)

I think I'm very prone to make the wrong conclusions
without see the whole picture.
Maybe that piece of ~~shit~~code
that appears to be irremediably moronic
is in there due to some strange historical reasons,
and the first "code reading" that I do aim to do just that:
get me in a position where the code changes
are in a context that I understand a little bit more about.

So *really*® read the PR before make any comments
is something that works very well for me (I guess).

### Enphasize the goods before bashing the bads

As alien as that concept may appear
the main concern of the code reviewer
should be to emphasize the good stuffs,
so they keep poping up.
IMHO this is much more effective
to avoid bad coding from "happen"
than just complain when it happens.
And no worries or false hopes:

#### _bad code will happen_

But relax,
now it's time to appreciate the good stuffs.
Again, since this is a difficult thing for us programmers
(should I dare to say humans?),
here are some examples
that I learnt from time and I use
(a variation of when makes sense)
on my reviews:

 - Nice idea in here! I didn't know this was possible.
 - Wow, this usage of _this_ blew me away,
I'll use this next time I have the same problem to solve.
 - Clever placement here, huh?
 - How have a I lived until now without knowing it!? 😱

And of course,
I hereby grant the permission
for you to use any kind of memes and animated gifs here.
Slow claps is one of my all time favorites.

### Reviews are historical registers

Githubz and similars
offer a great deal of tooling to make the code review
comments/messages look pretty and organized.
And I find myself more and more refering to "old" Pull Requests.
Majority of times to remember the suggestions
that arrived on solving some specific problem,
or changing some specific type of code.

Use (write them) as if someone (probably you)
would go back to it in the future.
This also should be kept in mind
while creating the Pull Requests,
but this is subject to a _whole new blog post_™.


#### Now, it's that time...

You SHOULD, or even: IS OBLIGATED to
point everything that is not ok with the Pull Request.
But I believe this should be done in the
most polite way that you think about.

I think a important thing to keep in mind before start
to point the things that should be different is:

#### _bad code will happen_

And this is totally fine.
We make mistakes all the bloody time, and we should,
otherwhise we are not trying anything new/better, right?

To point those problems create opportunities to assess why this is happening:
 - Something is unclear about our standards?
 - There is some business logics misconceptions?
 - Someone could enjoy some brown bag sessions on OO design?

##### Never say that something is plain ugly

First because it's just wrong. Don't be an ~~asshat~~ ~~douche~~ bad person.
But also because this is very, VERY subjective, right.

The pretty is in the viewers eyes.

So I try my best to be VERY objective about it.

##### When something is wrong, you should say why
(Github) Markdown is amazing to create really readable texts
with code syntax highlighting and everything.
I use it all the times in my comments.

And I allways try to give examples and
to use references to older experiences
(and even blog posts, books, etc).

I think here the main idea is:
try and prove your point.

When I **feel** that something is wrong
but I can't provide a clear example on how to do it better,
I try to call for a conversation.
Maybe then some idea arrives, but not in the _PR_.
Remember: I treat it as historical register. =)

##### When you "THINK" something is wrong, just test it first
I'm always watching myself to punch me in the right ear
before I write something like:

_"I guess this isn't really necessary, I'm not sure."_

The person that wrote the code spent some time on it,
wrote tests/specs to guarantee that it's working.
So I think it's just lame to "just guess"
that something in the PR isn't the best/right way to go.
And more than that,
kinda delegate all the job to prove or disprove something
to the same person that is working hard on some feature.

And in the majority of the times
I discover really nice stuff when I do a rapid test in the terminal.
You know? I'm talking about those
"`#third` method is on _Active Support_ or _Ruby_ itself " type of questions.

## References:

 + [github]()
 + [brown bag sessions]()
