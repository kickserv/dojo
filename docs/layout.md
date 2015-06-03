---
layout: page
title: Layout
---

Dojo's layout is a complex beast based partly on Zurb's Foundation for Apps [flexbox grid](http://foundation.zurb.com/apps/docs/#!/grid). Implementation of the layout is fairly straightforward, as you'll see below.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## App Grid

You can find all the below styles in `_grid.scss`.

You'll want to contain all of your UI elements in the space of the window, and then make certain sections of the app scrollable. To achieve this, wrap your entire app in a grid frame:

{% highlight html %}
<div class="grid-frame">
  <div class="grid-block"></div>
  <div class="grid-block"></div>
</div>
{% endhighlight %}

The app frame always takes up 100% of the width and 100% of the height of the user's browser window.

### Grid Blocks

Blocks are the... building blocks of Dojo. They're flexbox-powered elements that can be intelligently sized, re-oriented, and re-ordered.

#### Automatic sizing

You're probably used to pairing grid classes with sizing classes, like `.col-sm-6`, `.col-md-4`, and so on. In Dojo, when grid blocks don't have sizing classes, they take up an even amount of space.

{% example html %}
<div class="grid-block">
  <div class="grid-block"></div>
  <div class="grid-block"></div>
</div>
{% endexample %}

{% example html %}
<div class="grid-block">
  <div class="grid-block"></div>
  <div class="grid-block"></div>
  <div class="grid-block"></div>
</div>
{% endexample %}

#### Shrinking

While these blocks expand to fill available space, it's also possible to have a block shrink, which means it only takes up as much space as its content needs. This is useful for title bars, tabs, or any other content that's secondary to the main content area.

{% example html %}
<div class="grid-block">
  <div id="tabs" class="grid-block shrink">Such shrink</div>
  <div id="main" class="grid-block"></div>
</div>
{% endexample %}

#### Manual Sizing

It's also possible to size the grid using column-based sizing classes. The Dojo App Grid uses a 12-column grid, but you can change this by modifying the `$total-columns` variable in your settings file.

{% example html %}
<div class="grid-block">
  <div id="sidebar" class="medium-4 grid-block"></div>
  <div id="content" class="medium-8 grid-block"></div>
</div>
{% endexample %}

#### Parent-level Sizing

Lastly, the sizing of blocks can be set on the parent, rather than individual children. Add the class `[size]-up-[n]` to a parent block to automatically size all children to be the same width. `[size]` is a breakpoint, like `small` or `medium`, and `n` is the number of items to fit on each row. By default, `n` only goes up to six, but this can be changed by modifying the `$block-grid-max-size` variable in your settings file.

{% example html %}
<div class="grid-block small-up-3">
  <div class="grid-block"></div>
  <div class="grid-block"></div>
  <div class="grid-block"></div>
  <div class="grid-block"></div>
  <div class="grid-block"></div>
  <div class="grid-block"></div>
</div>
{% endexample %}

### Content Blocks

If basic blocks are the rows of a Foundation for Apps layout, then content blocks are the columns. They can be sized and re-ordered just like normal blocks, but they're meant to house actual content, not just more blocks.

{% highlight html %}
<div class="grid-block">
  <div class="grid-block">
    <div class="grid-content"></div>
    <div class="grid-content"></div>
  </div>
  <div class="grid-content"></div>
</div>
{% endhighlight %}

In the above example, you can see that `grid-content` elements are the bottommost elements of the basic layout. Use `grid-block` when you intend to keep nesting more blocks for your layout, and use `grid-content` when you're filling the element with "normal" content, like lists, text, tabs, or menus.

### The Vertical Grid

By default, blocks in a grid are layed out horizontally. A grid can be reoriented to be vertical by adding the `vertical` class to a parent element.

{% example html %}
<div class="vertical grid-block">
  <div class="grid-block"></div>
  <div class="grid-block"></div>
</div>
{% endexample %}

This behavior doesn't cascade down to child blocks—they'll be horizontal by default also.

You can also reorient the grid at different screen sizes by using adding breakpoint names to the classes.

{% example html %}
<div class="vertical medium-horizontal grid-block">
  <div class="grid-block"></div>
  <div class="grid-block"></div>
</div>
{% endexample %}

### More Examples

Find more examples and options at the Foundation for Apps [grid documentation](http://foundation.zurb.com/apps/docs/#!/grid).

## Content Grid

You can find all the below styles in `_layout.scss`.

The Content Grid can be used for more "traditional" content layout. It should be used inside a `.grid-content`.

### How it works

The grid is pretty standard—you create rows with `.columns` and individual columns with a column class and fraction class. Here's how it works:

- Add a `.container` to encapsulate everything and provide ample horizontal gutter space.
- Create your outer row to clear the floated columns with `<div class="columns">`.
- Add your columns with individual `<div class="column">`s.
- Add your fractional width classes to set the width of the columns (e.g., `.one-fourth`).

### Demo

In practice, your columns will look like the example below.

{% example html %}
<div class="container">
  <div class="columns">
    <div class="one-fifth column">
      .one-fifth
    </div>
    <div class="four-fifths column">
      .four-fifths
    </div>
  </div>

  <div class="columns">
    <div class="one-fourth column">
      .one-fourth
    </div>
    <div class="three-fourths column">
      .three-fourths
    </div>
  </div>

  <div class="columns">
    <div class="one-third column">
      .one-third
    </div>
    <div class="two-thirds column">
      .two-thirds
    </div>
  </div>

  <div class="columns">
    <div class="one-half column">
      .one-half
    </div>
    <div class="one-half column">
      .one-half
    </div>
  </div>
</div>
{% endexample %}

### Centered

Columns can be [centered](/utilities/#centering-content) by adding `.centered` to the `.column` class.

{% example html %}
<div class="columns">
  <div class="one-half column centered">
    .one-half
  </div>
</div>
{% endexample %}
