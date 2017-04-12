---
layout: post
title:  "O Code Review Maroto"
date:   2017-04-06 14:49:00
excerpt: Code Review é uma excelente oportunidade para ensinar e aprender na
mesma proporção.
description: "Code Review: uma excelente oportunidade para ensinar e aprender na
mesma proporção."
image: /images/polite-code-reviewer/buddha-try-to-not-be-an-asshat.jpg
categories:
  - en
  - working-with-others
---

### TL;DR

 - Code Review é uma oportunidade para ensinar
e aprender na mesma proporção.
 - Não comente antes de entender as motivações que levaram a uma mudança.
 - Gaste a mesma energia para reconhecer as coisas boas
(encorajando e elogiando isso)
que é gasta para encontrar coisas ruins.
 - Discussões em um code review geram material de estudo
(and podem servir para futuras referências).
 - Seja específico com que não está tão bom assim
e sempre códigos para exemplificar o que pode ser melhor.
 - Reconheça o esforço que o autor original empenhou
em fazer o melhor que ele pôde.

![Buddha says: try to not be an asshat](/images/polite-code-reviewer/buddha-try-to-not-be-an-asshat.jpg){: .center-image }

## Que negócio é esse aqui, bicho!? OMG!

Seguinte... tem um tempinho que alguns colegas vem me dizendo
que meus code reviews são um pouco "diferentes".
Sendo o rei da auto-estima que sou,
Comecei a me perguntar (e a perguntar para todo mundo)
o que eu estava fazendo errado, então.
Aí, para minha imensa surpresa,
descobrir que o "diferente" nesse caso
era na verdade algo batuta.

Eu vou tentar mostrar os passos que sigo
e também processo mental
que tenho usado em meus code reviews ultimamente.

### Read the code (_and not "just" the diff_ )

At least for me it's very tempting to just glance my eyes over the _diff_.
And I normally try my best to avoid this urge
and *really*® read the changes.

This is how I understand the context for the changes,
and I think this is a pre-condition
to make up any type of conclusions.

#### The objective here is to bring up the motivations

 - Why something is writen in the way it is?
 - What was the thought process the developer used here?
 - Can I learn something from it?
  (not just technically but even about the business?)

Maybe that piece of ~~shit~~ code
that appears to be irremediably moronic
is in there due to some strange historical reasons.
And the first "code reading" that I do
aim to do just that:
get me in a position where the code changes
are wrapped in a context that fits in my mind.

So to *really*® read the PR before post any comments
is something that works very well for me (I guess).

### Emphasize the goods before bashing the bads

As alien as that concept may appear I really (want to) believe that
the main concern of the code reviewer is to emphasize the good stuffs.
This way those can find the atmosphere to they keep poping up.

![WOOOW! Just blewed me away. Wink!](/images/polite-code-reviewer/wow-wink.gif){: .center-image }

IMHO it's much more effective to avoid bad coding from "happening"
than just complain when it happens.
And no worries or false hopes:

#### _bad code is going "to happen"_

But my advice is: just relax
and focus the review on appreciation of the good stuffs.
Again, since this is a difficult thing for us programmers
(should I dare to say humans?),
here are some examples that Time taught me
and that I tend to mix, match and use on my reviews:

 - Nice idea in here! I didn't know this was possible.
 - Wow, this usage of _this_ blew me away,
I'll use it next time I have the same problem to solve.
 - Clever placement here, huh?
 - How have a I lived until now without knowing it!? 😱

And of course, I hereby grant the permission
for you to use any kind of memes and animated gifs in this phase.
Slow claps is one of my all time favorites.

![Here some slow claps: you sure deserve it!](/images/polite-code-reviewer/slow-claps.gif){: .center-image }

### Reviews are historical registers

Githubz and similars offer a great deal of tooling
to make the code review comments/messages look pretty and organized.
And I find myself more and more referring to "old" Pull Requests.
Majority of the times to remember the suggestions
that arrived on solving some specific problem,
or changing some specific type of code.

Write them as if someone,
much probably you,
would go back to it in the future.
This also should be kept in mind
while creating the Pull Requests,
but this is subject to a _whole new blog post_™.

### Now, it's that time...

I try my best to point everything
that is not ok with the Pull Request.
But I believe this should be done in the
most polite way that I can.
And let's face it already: I'm a sir.

An important thing to keep in mind
(before start to point the things that should be different)
is:

#### _bad code **is going "to happen"**_, remember?

And this is totally fine.
We make mistakes all the bloody time.
Well, at least I do.
MAYBE I'M A MORON, WHO KNOWS!?
But seriously, if we don't make booboos
we are not trying anything new/better, right?

To point those problems is
to create opportunities to assess why this is happening:
 - Something is unclear about our standards?
 - There is some business logic misconceptions?
 - Someone could enjoy some brown bag sessions on OO design?

#### Never say that something is plain ugly

First because it's just wrong.
Don't be an ~~asshat~~ ~~douche~~ bad person.
But also because this is very, VERY subjective.

_The prettyness is in the viewers eyes._

So I try my best to be VERY objective about it.

##### If something is wrong, I try to show why and how

I use the miracle of code syntax highlighting
and all sorts of _h1_, _h2_ and _h3_ on my markdowns
to make my comments very readable.
Well... at least I try, ok!? 😤

Another tip is to enhance the examples
with references to older experiences,
other people on the interwebz that the team respect
(blog posts, books, etc).

_Try and prove your point.
Do some effort.
Spent some time on it._

When I **feel** that something is wrong
but I can't provide a clear example on how to do it better,
I try to call for a conversation.
You know? That old thing when you
exchange some words? Face to face?
Probably some ideas will pop up,
but I really avoid to write in the _PR_ those foggy brain farts💨.

##### When you "THINK" something is wrong, just test it first

I'm always watching myself to punch me in the right ear
before I write something like:

_"I guess this isn't really necessary, ya know?
But I'm, like, not sure."_

The person that wrote the code spent some time on it,
thought about some abstractions to make it cool,
wrote tests/specs to guarantee that it's working...
So I think it's just lame to "just guess"
that something in the PR isn't the best/right way to go.
And more than that,
kinda delegate all the job to prove or disprove
something to the same person
that is working hard on some feature.

And in the majority of the cases
I discover really nice stuff when I do a rapid test in the terminal.
You know? I'm talking about those
"`#third` method is on _Active Support_ or _Ruby_ itself "
type of questions.

![It was TOTALLY worth it. Even with all the punchs directly at the nose.](/images/polite-code-reviewer/worth-it.jpg){: .center-image }

## Now go there and just enjoy your day

We are all here for the fun and the learnings.
So hang around with your peers allways you can,
talk about what you can do better
to improve your interactions.

Let's have some fun on our working lifes.

xoxo

## Thank you very much. REALLY! BIG THANKS

This post would be even worst
without the carefull early reading, revision
and polite point fingers from

 - [@hosseintoussi](https://github.com/hosseintoussi)

You are the man, bruv! 💙

## References:

 + [github](http://github.com)
 + [brown bag sessions](https://www.quora.com/What-is-a-brown-bag-session)
