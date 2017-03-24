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
I started to ask which could I do to make them better.
For my huge surprise,
the "different" in this scenario
was a very good thing.
So I'll try to break down into steps
the though process
that make me review code
the way I do nowadays.

### Read the code (_and not "just" the diff_ )

At least for me is very tempting
to just glance my eyes over the _diff_.
What I'm trying to say here is that
I normally avoid this.
I try to *really*® read the change
and understanding the motivations
before make up any type of conclusions.

It's very prone to make the wrong ones (conclusions)
without see the whole picture.
Maybe that piece of ~~shit~~ code that
appears to be irremediably moronic
is there due to some strange historical motive.
I'm not saying that it shouldn't be pointed,
but maybe even the way we point it
will change dramatically knowing why it's there.

So *really*® read the PR before make any comments
is something that works very well for me
in the sense that it sometimes changes completely
my understanding about why I'll talk about.


### Reviews are historical registers

Use (write them)
as if someone (even you)
would go back to it in the future
to understand what happened in a specific day/change.
This also should be kept in mind
while creating the pull request,
but this is subject to a whole new blog post.

### Enphasize the goods before bashing the bads

As alien as it may appear
the main concern of the code reviewer
should be to emphasize the good stuffs,
so they keep poping up.

#### Now, bash the bads as hell

You SHOULD,
or even: IS OBLIGATED to
bash the not so fine stuff.
But I believe in a proper way to do this.

##### Never say that something is plain ugly
##### When something is wrong, you should say how
Github markdown and all of it
is amazing to create really readable texts
with code syntax highlighting and everything.
So use it.
Give examples,
use references to older experiences and blog posts.
Try and prove your point.
