---
layout: simple
title: About
---

Learn more about this styleguide, particularly how it's built and who maintains it.

### What and why

Dojo is Kickserv's internal CSS framework. It includes basic global styling for typography, small components like buttons and tabs, and our general guidelines for writing HTML and CSS.

Open-sourcing Dojo means sharing and learning with the community. There's a lot we can improve upon in Dojo, and help is always appreciated. While we don't currently plan on building this out as a competitor to other front-end frameworks, we will occasionally add, remove, or modify things.

### Libraries in Use

Dojo takes inspiration (and code) from the following open source libraries.

* [Bootstrap](http://getbootstrap.com)
  * Code licensed under the [MIT License](https://github.com/twbs/bootstrap/blob/master/LICENSE)
  * Documentation licensed under [CC BY 3.0](https://github.com/twbs/bootstrap/blob/master/docs/LICENSE)
  * Designed and built by [@mdo](http://twitter.com/mdo) and [@fat](http://twitter.com/fat)
  * Copyright 2011-2015 Twitter, Inc.
* [Font Awesome](http://fortawesome.github.io/Font-Awesome/)
  * Code licensed under the [MIT License](http://opensource.org/licenses/mit-license.html)
  * Documentation licensed under [CC BY 3.0](http://creativecommons.org/licenses/by/3.0/)
  * Fonts licensed under the [OFL License](http://scripts.sil.org/OFL)
* [Foundation for Apps](http://foundation.zurb.com/apps)
  * Licensed under the [MIT License](https://github.com/zurb/foundation-apps/blob/master/LICENSE)
  * Copyright 1998-2015 Zurb, Inc.
* [Github Octicons](http://octicons.github.com)
  * Code licensed under the [MIT License](https://github.com/github/octicons/blob/master/LICENSE.txt)
  * Fonts licensed under the [OFL License](https://github.com/github/octicons/blob/master/LICENSE.txt)
* [Github Primer](http://primercss.io/)
  * Licensed under the [MIT License](https://github.com/primer/primer/blob/master/LICENSE.md)
  * Copyright 2015 GitHub, Inc.

### Browser support

Dojo currently supports Internet Explorer 10+ and the latest two versions of Chrome, Safari, and Firefox on OS X and Windows.

### Dependencies

- Our styles are built with SCSS.
- Bower is used to link Markdown styles.
- Autoprefixer is used to generate vendor-prefixed declarations and is handled via our Gruntfile.
- A custom plugin for snippet and example combos, `example.rb`, was created as a fork of Jekyll's built-in `highlight` plugin.

### Who

Currently maintained by [@briannelsondsgn](https://twitter.com/briannelsondsgn) and the Kickserv front-end team.
