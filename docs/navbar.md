---
layout: page
title: Navbar
---

Dojo comes with a navbar custom-designed for Kickserv.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Main Navbar

The main navbar contains the Kickserv logo, main app sections, and account menu. The default presentation of the navbar is vertical, to be used as a sidebar.


{% example html %}
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
</div>
{% endexample %}

### Horizontal Navbar

You can easily change the layout of the navbar by using a `.navbar-top` class on the `body`.

**Note:** We're not using a `body` in this example because it would mess up the page rendering!

{% example html %}
<div class="navbar-top">
  <div class="grid-frame">
    <div class="navbar">
      <div class="navbar-brand">
        <a href="/" class="brand">
          <img src="/img/nav_icon.svg" />
        </a>
      </div>
      <div class="navbar-utility">
        <a href="" class="utility">
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
    </div>
  </div>
</div>
{% endexample %}

## Subnav

On certain pages, it may be necessary to include a subnav bar. Use the following structure and include as necessary.

{% example html %}
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
</div>
{% endexample %}
