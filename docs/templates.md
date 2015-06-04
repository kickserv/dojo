---
layout: page
title: Templates
---

Best practices and guidelines for writing HTML and CSS with approachable formatting, syntax, and more.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Rails Layout

This is a master layout for use in Kickserv. The navbar can be easily switched from horizontal to vertical by adding and removing `.vertical` from the `.grid-frame`.

**Note:** Adding `.vertical` makes the navbar *horizontal*, since the `.vertical` class tells the contained `.grid-block` divs to be stacked *vertically*. Confusing, I know.

{% highlight erb %}
<!DOCTYPE html>
<html lang="en">
  <head>
    ...
  </head>

  <!-- Add or remove .navbar-top to body to toggle horizontal navbar-->
  <body>
    <div class="grid-frame">
      <div class="navbar">
        ...
      </div>

      <div class="grid-block vertical" id="content">
        <div class="subnav">
          ...
        </div>
        <div class="grid-block">
          ...
        </div>
      </div>
    </div>
  </body>
</html>
{% endhighlight %}
