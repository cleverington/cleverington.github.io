---
layout: post
title:  "Tweaking GitHub Pages"
date:   2017-10-13 23:35:06
categories: blog jekyll learning github-pages
---

# Tweaking GitHub Pages

## Background

As part of my ongoing contributions to the Drupal Community (and doing my part for global activism), I recently did a lot of work with the Drupal Diversity and Inclusion Workgroup on getting their page at drupaldiversity.github.io 'up to par'.

Top on the goals were
- **Accessibility**
- **Availability**

## Accessibility

The Accessibility was probably *easier*, because we were using a minimalistic theme with a rather simplistic interface.

The trick was ensuring we had little violation of the Color Contrast Requirements as required by WCAG 2.0. 

As you might have noticed while reading on **THIS** site, I did some playtesting with adding a button to enforce the [Open Dyslexic](opendyslexic.org "Open Dyslexic") font via the `! important` tag and some CSS3 on the whole site.

Adding it to the site however, would have required inclusion via a `fonts/` folder, which we were trying to avoid so long-term site maintenance is kept at a minimum. Especially with how easy it is to instead just add a CDN from Google Fonts.

Adding a Google Font just requires googling "Google Fonts", selecting the font, and getting the Import. Customization is even available to allow *choosing* which pieces of the Font a site-designer wishes to use.

There are definitely better approaches, but live and learn.

## Availability

Availability meant one thing first: Search Engine Optimization (SEO)

For good showcasing, that meant having SEO Tags available and having a Feed available to host on DrupalPlanet.

### The Problem: A Dated Gemfile

Now, for those who have used a GitHub Pages setup previously, the base Gemfile requires literally **nothing** to get started:
```ruby
source 'https:rubygems.org'
gem 'github-pages', group: :jekyll_plugins
```

By default, GitHub Pages sets all new "Sites" up with Minima as a theme, unless another is selected. So, theoretically, hidden somewhere "Upstream" is a line of code reading this:
`gem "minima", "~> 2.0"`

Some of the newer GitHub Pages created sites however, have a slightly different (and way better) Gemfile:
```ruby
source 'https://rubygems.org'

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
# gem "jekyll", "3.3.0"

# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "minima", "~> 2.0"

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
# group :jekyll_plugins do
# end
```
As can be seen, Documentation makes the world a better place.

> If it isn't documented, it doesn't exist. ~~ Nicholas Zakas

### The Updated Gemfile

As can be seen on the Gemfile for this site (at https://github.com/cleverington/cleverington.github.io/blob/master/Gemfile), all it took to 'boost' the SEO from a configuration standpoint was a very small alteration:

```ruby
group :jekyll_plugins do
   gem "jekyll-feed"
   gem "jekyll-seo-tag"
   gem "jekyll-sitemap"
end
```
The SiteMap is pending for a future tweak, but the site started to get out there and **that** was the most important thing.

### Other Plugins

See https://pages.github.com/versions/ for a list of the available Jekyll plugins available on GitHub for GitHub Pages hosted sites.

### Look me up

> "No man is an island." ~ John Donne \(1624\)

If there's a mistake, let me know.
If I can make it better, let me know.

#### Thoughts, recommendations, good recipes for cooking pumpkin:

[Twitter - @c_leverington](https://twitter.com/c_leverington)
[github - cleverington](https://github.com/cleverington/n00b-drupal-development)
[d.o - cleverington](https://www.drupal.org/u/cleverington)
