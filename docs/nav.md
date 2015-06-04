---
layout: page
title: Navigation
---

Dojo comes with several navigation components. Some were designed with singular purposes, while others were design to be more flexible and appear quite frequently.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Navbar

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

## Menu

The menu is a vertical list of navigational links. **A menu's width and placement must be set by you.** If you like, just use our grid columns as a parent. Otherwise, apply a custom `width`.

{% example html %}
<nav class="menu">
  <a class="menu-item selected" href="#">Account</a>
  <a class="menu-item" href="#">Profile</a>
  <a class="menu-item" href="#">Emails</a>
  <a class="menu-item" href="#">Notifications</a>
</nav>
{% endexample %}

There are a few subcomponents and add-ons that work well with the menu, including avatars, counters, and Octicons.

{% example html %}
<nav class="menu">
  <a class="menu-item selected" href="#">
    <span class="octicon octicon-tools"></span>
    Account
  </a>
  <a class="menu-item" href="#">
    <span class="octicon octicon-person"></span>
    Profile
  </a>
  <a class="menu-item" href="#">
    <span class="octicon octicon-mail"></span>
    Emails
  </a>
  <a class="menu-item" href="#">
    <span class="octicon octicon-radio-tower"></span>
    <span class="counter">3</span>
    Notifications
  </a>
</nav>
{% endexample %}

You can also add optional headings to a menu. Feel free to use nearly any semantic element with the `.menu-heading` class, including inline elements, headings, and more.

{% example html %}
<nav class="menu">
  <span class="menu-heading">Menu heading</span>
  <a class="menu-item selected" href="#">Account</a>
  <a class="menu-item" href="#">Profile</a>
  <a class="menu-item" href="#">Emails</a>
  <a class="menu-item" href="#">Notifications</a>
</nav>
{% endexample %}


## Tabnav

When you need to toggle between different views, consider using a tabnav. It'll given you a left-aligned horizontal row of... tabs!

{% example html %}
<div class="tabnav">
  <nav class="tabnav-tabs">
    <a href="#" class="tabnav-tab selected">Foo tab</a>
    <a href="#" class="tabnav-tab">Bar tab</a>
  </nav>
</div>
{% endexample %}

Use `.right` to align additional elements in the `.tabnav`:

{% example html %}
<div class="tabnav">
  <a class="btn btn-sm right" href="#">Button</a>
  <nav class="tabnav-tabs">
    <a href="#" class="tabnav-tab selected">Foo Tab</a>
    <a href="#" class="tabnav-tab">Bar Tab</a>
  </nav>
</div>
{% endexample %}

Additional bits of text and links can be styled for optimal placement with `.tabnav-extra`:

{% example html %}
<div class="tabnav">
  <div class="tabnav-extra right">
    Tabnav widget text here.
  </div>
  <nav class="tabnav-tabs">
    <a href="#" class="tabnav-tab selected">Foo Tab</a>
    <a href="#" class="tabnav-tab">Bar Tab</a>
  </nav>
</div>
{% endexample %}

{% example html %}
<div class="tabnav">
  <div class="right">
    <a class="tabnav-extra" href="#">
      Tabnav extra link
    </a>
    <a class="tabnav-extra" href="#">
      Tabnav extra link
    </a>
  </div>
  <nav class="tabnav-tabs">
    <a href="#" class="tabnav-tab selected">Foo Tab</a>
    <a href="#" class="tabnav-tab">Bar Tab</a>
  </nav>
</div>
{% endexample %}

## Filter list

A vertical list of filters. Grey text on white background. Selecting a filter from the list will fill its background with blue and make the text white.

{% example html %}
<ul class="filter-list">
  <li>
    <a href="#" class="filter-item selected">
      <span class="count">21</span>
      First filter
    </a>
  </li>
  <li>
    <a href="#" class="filter-item">
      <span class="count">3</span>
      Second filter
    </a>
  </li>
  <li>
    <a href="#" class="filter-item">
      Third filter
    </a>
  </li>
</ul>
{% endexample %}
