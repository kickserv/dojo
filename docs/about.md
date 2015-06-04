---
layout: simple
title: About
---

Learn more about this styleguide, particularly how it's built and who maintains it.

### What and why

Dojo is Kickserv's internal CSS framework. It includes basic global styling for typography, small components like buttons and tabs, and our general guidelines for writing HTML and CSS. It's been used internally at Kickserv for years now.

Open-sourcing Dojo means sharing and learning with the community. There's a lot we can improve upon in Dojo, and help is always appreciated. While we don't currently plan on building this out as a competitor to other front-end frameworks, we will occasionally add, remove, or modify things.

### Libraries in Use

Dojo takes inspiration (and code) from the following open source frameworks.

* [Foundation for Apps](http://foundation.zurb.com/apps)
  * App Grid
* [Bootstrap](http://getbootstrap.com)
  * Pagination
  * Responsive Embed
* [Github Primer](http://primercss.io/)
  * Everything Else

### Browser support

Dojo currently supports Internet Explorer 10+ and the latest two versions of Chrome, Safari, and Firefox on OS X and Windows.

### Dependencies

- Our styles are built with SCSS.
- Bower is used to link Kickserv assets, namely Github's [Octicons](http://octicons.github.com) icon font and Markdown styles.
- Autoprefixer is used to generate vendor-prefixed declarations and is handled via our Gruntfile.
- A custom plugin for snippet and example combos, `example.rb`, was created as a fork of Jekyll's built-in `highlight` plugin.

### Who

Currently maintained by [@briannelsondsgn](https://twitter.com/briannelsondsgn) and the Kickserv front-end team.
