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

  <body class="ks-app">

    <!-- Add or remove .vertical to toggle horizontal navbar-->
    <div class="grid-frame vertical">

      <!-- Navbar -->
      <div class="grid-block shrink" id="navbar">
        <div class="grid-block shrink">
          <div class="grid-content ks-logo text-center">
            <a href="/">
              <%= image_tag "connect/nav_icon.svg", class: "ks-logo", alt: "Connect", height: "54" %>
            </a>
          </div>
        </div>
        <div class="grid-block" id="ks-nav">
          <div class="grid-content ks-nav">
            Main Nav Choices
          </div>
        </div>
        <div class="grid-block shrink">
          <div class="grid-content ks-usernav">
            <a href="#usernav" class="js-dropdown-toggle">
              <%= employee_avatar(current_user) %>
              <span class="ks-usernav-name"><%= current_user.name %></span>
            </a>
          </div>
        </div>
      </div><!--#navbar-->

      <!-- Main Content -->
      <div class="grid-block vertical" id="content">
        <%= yield(:subnav) %>
        <div class="grid-block ks-content-block">
          ...
        </div>
      </div><!--#content-->

    </div><!--.grid-frame-->

  </body>
</html>
{% endhighlight %}
