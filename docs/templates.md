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
  <body class="ks-app">
    <div class="grid-frame">

      <div class="navbar">
        <div class="navbar-brand">
          <a href="/" class="brand">
            <img src="/img/nav_icon.svg" />
          </a>
        </div>
        <div class="navbar-utility">
          <a href="#usernav" class="utility js-dropdown-toggle">
            <img class="avatar avatar-small" src="https://avatars3.githubusercontent.com/u/9919?v=3&s=32" width="30" height="30">
            <span class="utility-name">Brian Nelson</span>
          </a>
        </div>
        <div class="navbar-menu">
          <ul class="nav">
            <li>
              <a href="">
                <i class="octicon octicon-clippy"></i>
                <span class="nav-label">Estimates</span>
              </a>
            </li>
            <li class="active">
              <a href="">
                <i class="octicon octicon-briefcase"></i>
                <span class="nav-label">Jobs</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="octicon octicon-organization"></i>
                <span class="nav-label">Contacts</span>
              </a>
            </li>
          </ul>
        </div>
      </div><!--.navbar-->

      <div class="grid-block vertical" id="content">

        <div class="subnav">
          <div class="grid-block">
            <div class="grid-content">
              <ul class="nav">
                <li class="active">
                  <a href="/schedule">
                    Agenda
                  </a>
                </li>
                <li>
                  <a href="/calendar">
                    Calendar
                  </a>
                </li>
              </ul>
            </div>
          </div>
          <div class="grid-block shrink">
            <div class="grid-content">
              <button type="button" class="btn btn-action btn-sm new-event">New Event</button>
            </div>
          </div>
        </div><!--.subnav-->

        <div class="grid-block">
          ...
        </div>

      </div><!--#content-->
    </div><!--.grid-frame-->
  </body>
</html>
{% endhighlight %}
