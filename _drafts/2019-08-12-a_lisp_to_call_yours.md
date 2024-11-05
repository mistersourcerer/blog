---
layout: post-comments
title:  A lisp to call yours (in Ruby) [S01E??]
//date:   
excerpt: OMG LOL
description: BBQ
image: /images/polite-code-reviewer/buddha-try-to-not-be-an-asshat.jpg
categories:
  - en
  - learning-by-doing
tags:
  - lisp
  - language-design
  - writing-a-language
  - interpreters
  - functional-programming
  - linked-list
---

### TL;DR

Let's write a programming language in Ruby!
A functional and interepreted one.
It is going to be a Lisp dialect, to be very precise.

[I can't wait, bring it on!](#to-program-is-to-concatenate-strings)!

We are going to write it in Ruby
and I am pretty sure
you could use the same ideas and steps
to build this or other lisp dialect in any language.

This is the first part of a series where you will:

  - create a new Ruby gem/project
  - make a basic interpreter that recognizes double quoted strings
  - use the interpreter in a brand new REPL. Yes, you are going to write one!
  - update your interpreter so it also recognizes numbers
  - and what about lists? Well... first you need a List to call yours (ok, last time I use this phrase!)

## To program is to concatenate strings

I didn't said that. And I don't know who did.
But it is truthy.

So let's start by recognizing a string.
Come back here after you create a new gem,
mine will be called `lispoor`.

If you need help to create your Ruby project,
[I got you covered](#get-preped)!


## Get Preped!

<div class="image-box">
	<img src="/images/lbd/lisp/docbrown.jpg" />

	<span class="text">
		These are the versions I am using here.
		Just in case you are reading it after take
		a quick trip to the future or something.
	</span>
</div>


```bash
➜ ruby -v
ruby 2.6.3p62 (2019-04-16 revision 67580) [x86_64-darwin18]

➜ bundle -v
Bundler version 2.0.2

➜ bundle gem lispoor
Creating gem 'lispoor'...
MIT License enabled in config
      create  lispoor/Gemfile
      create  lispoor/lib/lispoor.rb
      create  lispoor/lib/lispoor/version.rb
      create  lispoor/lispoor.gemspec
      create  lispoor/Rakefile
      create  lispoor/README.md
      create  lispoor/bin/console
      create  lispoor/bin/setup
      create  lispoor/.gitignore
      create  lispoor/.travis.yml
      create  lispoor/.rspec
      create  lispoor/spec/spec_helper.rb
      create  lispoor/spec/lispoor_spec.rb
      create  lispoor/LICENSE.txt
```

### Extra mile

The previous output can be different in your case.
Here you have my `~/.bundle/config` for comparison:

```bash
➜ cat ~/.bundle/config
---
BUNDLE_GEM__TEST: "rspec"
BUNDLE_GEM__MIT: "true"
BUNDLE_GEM__COC: "false"
```

Also if you are following this step by step,
you might want to run a `bundle exec rake`
(or anything bundle related) to see and fix
every warning on your just created gemspec
will generate right now:

```
➜ bundle exec rake
bundler: failed to load command: rake (/.../.rbenv/versions/2.6.3/bin/rake)
Gem::InvalidSpecificationException: The gemspec at /.../lispoor/lispoor.gemspec is not valid. Please fix this gemspec.
The validation error was 'metadata['homepage_uri'] has invalid link: "TODO: Put your gem's website or public repo URL here."'
...
```
