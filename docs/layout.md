---
layout: page
title: Layout
---

Dojo's layout is a complex beast based partly on Zurb's Foundation for Apps [flexbox grid](http://foundation.zurb.com/apps/docs/#!/grid). Implementation of the layout is fairly straightforward, as you'll see below.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## App Frame

You'll want to contain all of your UI elements in the space of the window, and then make certain sections of the app scrollable. To achieve this, wrap your entire app in a grid frame:

{% highlight html %}
<div class="grid-frame">
  <div class="grid-block"></div>
  <div class="grid-block"></div>
</div>
{% endhighlight %}

The app frame always takes up 100% of the width and 100% of the height of the user's browser window.

## Grid Blocks

Blocks are the... building blocks of Dojo. They're flexbox-powered elements that can be intelligently sized, re-oriented, and re-ordered.

### Automatic sizing

You're probably used to pairing grid classes with sizing classes, like `.col-sm-6`, `.col-md-4`, and so on. In Dojo, when grid blocks don't have sizing classes, they take up an even amount of space.

{% example html %}
<div class="grid-block">
  <div class="grid-block">One Block</div>
  <div class="grid-block">Two Blocks</div>
</div>
{% endexample %}

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
