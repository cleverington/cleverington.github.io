---
layout: post
title:  "Back and Upgraded"
date:   2017-01-15 23:35:06
categories: blog jekyll learning gitpages
---

## Back and Upgraded

Okay, so working in Windows is possible, but everything is *smoother* and *faster* on OSX.

### Things Learned (and the long silence)

Don't Trust Bash in Windows on Win10-Home
=========================================

I actually tested the 'Bash in Windows' fairly heavily over the Summer and was not entirely impressed. (I will refer to it as Win-Bash from here on out.) It is basically a functional VM which remotely accesses the base-level Windows Kernel (as told by one of the Windows Developers at OSCON).

This sounds great, until you realize that it makes these calls, as I noted, within a tiny containerized VM.  This means those commands executed via Win-Bash are not available **by** Windows within the GUI. For example, MySQL commands can be executed, but only if going through this really odd step-by-step process to create an SSH to the Shell.

The downsides do not truly affect self-contained programs such as Git (which pretty much does its thing), until you wish to use a `git push`. Because of the 'container' running on the Kernel, it does not actually *use* the same SSH Keys like software such as Git-GUI or Git-Bash. For the savvy user this means maintaining two SSH Keys (in a *weird* setup) or only completing pushes from outside the Win-Bash.

Likewise on tools like Ruby, Jekyll, bower, Node, etc.

To Developer on Windows 10, get Pro
===================================

Sad to say, but its true.

Hyper-V, a really cool 'built-in' VM tool on Windows, is only available on Windows10 Pro. With Docker dropping Windows10-Home support (due to **requiring** Hyper-V to work on Windows), almost all of the Web-Dev tools I use for Windows have become questionably functional.

Okay, so you don't HAVE to have Pro
===================================

The following programs still work well on Windows-Home and make for a great local Developer's solution (when automation and Third-Party tools like SASS/SCSS, Grunt, Gulp, etc. aren't required).

- Node.js: It technically works and installs, but good-luck getting packages which don't got sideways at random times.
- PHPStorm: Its PHPStorm. It works. The only difference / downside the Dev will find between OSX and Windows is having PowerShell instead of iTerm.
- PowerShell: If you're going to use the Command Prompt and you learned on Bash, try http://cmder.net/. I have been told the PowerShell is pretty awesome, but my knowledge base is heavily within Bash Scripting, so the Cmder Bash-Emulator is a great tool.
- Visual Studio: Seriously, if you're going to Developer on Windows, get Visual Studio and run through some Microsoft University Tutorials. I've never really gotten into the ... *groove*... of Visual Studio, but it is a **massively** powerful IDE. Seriously. Baked/Built in Debugging, Testing, and Collaboration, while supporting a bunch of integrations with other packages like Microsoft SQL Server, Azure's .NET SDK, and tons more.

### Back on OSX

Bash-IT
=======

After giving it just over half a year Dev'ing on Windows, I'm back on OSX (for home Dev, never gave it up for work. I was testing, not **crazy**!!)

The first thing I found, which is amazing, is a little tool called [Bash-IT](https://github.com/Bash-it/bash-it "Bash-IT"). As a *"shameless ripoff of [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh "oh-my-zsh")"*, Bash-IT has enough 'out-of-the-box' Bash Configurations to suit anyone's flavor.


See https://github.com/Bash-it/bash-it/wiki/Themes for Available Bash-IT Themes.

### To Be Continued

### Look me up

> "No man is an island." ~ John Donne \(1624\)

If there's a mistake, let me know.
If I can make it better, let me know.

#### Thoughts, recommendations, good recipes for cooking pumpkin:

[Twitter - @c_leverington](https://twitter.com/c_leverington)
[github - cleverington](https://github.com/cleverington/n00b-drupal-development)
[d.o - cleverington](https://www.drupal.org/u/cleverington)
