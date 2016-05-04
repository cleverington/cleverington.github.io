---
layout: post
title:  "Testing Jekyll and New Directions"
date:   2016-05-03 19:18:06 -0500
categories: blog jekyll learning gitpages
---

## Jekyll Is Pretty Awesome
Okay, so a little testing with Jekyll has taught me a few things......

* 1 Making an independent theme for a subproject (aka: generating CSS separarte from my current theme): **Difficult**
* 2 Customizing the basic Jekyll-baked theme: **Intermediate**
* 3 Adding new posts: **Super-Easy**
* 4 Learning the *kramdown* version of *Markdown*: **Haven't bothered**
* 5 I like ice cream

Nope, I'm lying. I already knew I liked ice cream.

I will note that I tried three different pre-baked Jekyll themes and many of them required a good deal of Jekyll functionality just simply **not** supported by Git-Bash on Windows (specifically, Windows 10).

## A New Direction

Why am I on Windows, you ask?

Testing. To make a cross-platform learning environment means working cross-platform.

Thus, instead of recommending, for example, iTerm2 and a whole massive customization build with *Oh My Zsh*, *zsh*, etc., I will instead look at including that level of Power-User customization within an Appendix.

I still firmly believe that Drupal Content Authors, Front-End Developers, Back-End Developers, etc. will have the best *experience* on an up-to-date OSX or Linux OS, but many **n00bs** only have (and are only familiar with) Windows machines. It is what they grew up with at school, it is what they were trained on, and, most likely, what they took early Web Authoring classes on.

That's not to say that the n00b's Guide will change fundamentally. With the opportunities allowed by Git Branching, I may simply create a Branch-Structure like this:
```
--
  |_ 7.x-0.x-dev
  |_ 7.x-0.x-dev_windows
  |_ 7.x-0.x-dev_osx
  |_ 7.x-0.x-dev_linux
```
... and include all three operating systems.

I will need to decide at a later date if that is a viable route, becuase, with only a little thought on the topic, this is an *extremely* ambitious endeavor which can end very badly.

Along the way, however, I intend to explore different technologies that may/will allow for cross-functional Development, such as Jeff Geerling's [Drupal VM](http://www.drupalvm.com/ "Drupal VM").

**IF...** or perhaps, more truthfully, **WHEN** a cross-functional Development platform that is stable on Windows arises, expect me to blog about it here (after taking it for a test run).

> As a side-note here, the Drupal VM *does* work in Windows, and actually tends to work well, but pretty much requires a Quad-Core processor and at least 8gb of RAM. This means a knowledgeable user can build an *actual* Virtual Machine, then load up the Drupal VM (Ansible and all) headlessly within the Virtual Machine.

For example, Phase2's new project [DevTools](http://phase2.github.io/devtools/ "DevTools") *sounds* like a great Docker-machine project, but requires development on either a Linux or a Mac.



### Look me up

> "No man is an island." ~ John Donne \(1624\)

If there's a mistake, let me know.
If I can make it better, let me know.

#### Thoughts, recommendations, good recipes for cooking pumpkin:

[Twitter - @c_leverington](https://twitter.com/c_leverington)
[github - cleverington](https://github.com/cleverington/n00b-drupal-development)
[d.o - cleverington](https://www.drupal.org/u/cleverington)
