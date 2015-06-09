---
layout: page
title: Navigation
---

Dojo comes with several navigation components. Some were designed with singular purposes, while others were design to be more flexible and appear quite frequently.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Navbar

The main navbar contains the Kickserv logo, main app sections, and account menu.

### Vertical Navbar

The default presentation of the navbar is vertical, to be used as a sidebar.

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

## Toggleable Tabnav

### Example tabs

Add quick, dynamic tab functionality to transition through panes of local content.

{% example html %}
<div class="tabnav">
  <nav class="tabnav-tabs">
    <a href="#home" class="tabnav-tab active" data-toggle="tab">Home</a>
    <a href="#profile" class="tabnav-tab" data-toggle="tab">Profile</a>
    <a href="#third" class="tabnav-tab" data-toggle="tab">Third</a>
  </nav>
</div>

<div class="tab-content">
  <div class="tab-pane active" id="home">
    Raw denim you probably haven't heard of them jean shorts Austin. Nesciunt tofu stumptown aliqua, retro synth master cleanse. Mustache cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro keffiyeh dreamcatcher synth. Cosby sweater eu banh mi, qui irure terry richardson ex squid. Aliquip placeat salvia cillum iphone. Seitan aliquip quis cardigan american apparel, butcher voluptate nisi qui.
  </div>
  <div class="tab-pane" id="profile">
    Food truck fixie locavore, accusamus mcsweeney's marfa nulla single-origin coffee squid. Exercitation +1 labore velit, blog sartorial PBR leggings next level wes anderson artisan four loko farm-to-table craft beer twee. Qui photo booth letterpress, commodo enim craft beer mlkshk aliquip jean shorts ullamco ad vinyl cillum PBR. Homo nostrud organic, assumenda labore aesthetic magna delectus mollit. Keytar helvetica VHS salvia yr, vero magna velit sapiente labore stumptown. Vegan fanny pack odio cillum wes anderson 8-bit, sustainable jean shorts beard ut DIY ethical culpa terry richardson biodiesel. Art party scenester stumptown, tumblr butcher vero sint qui sapiente accusamus tattooed echo park.
  </div>
  <div class="tab-pane" id="third">
    Etsy mixtape wayfarers, ethical wes anderson tofu before they sold out mcsweeney's organic lomo retro fanny pack lo-fi farm-to-table readymade. Messenger bag gentrify pitchfork tattooed craft beer, iphone skateboard locavore carles etsy salvia banksy hoodie helvetica. DIY synth PBR banksy irony. Leggings gentrify squid 8-bit cred pitchfork. Williamsburg banh mi whatever gluten-free, carles pitchfork biodiesel fixie etsy retro mlkshk vice blog. Scenester cred you probably haven't heard of them, vinyl craft beer blog stumptown. Pitchfork sustainable tofu synth chambray yr.
  </div>
</div>
{% endexample %}

### Usage

Enable tabbable tabs via JavaScript (each tab needs to be activated individually):

$('#myTab a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})

You can activate individual tabs in several ways:

$('#myTab a[href="#profile"]').tab('show') // Select tab by name
$('#myTab a:first').tab('show') // Select first tab
$('#myTab a:last').tab('show') // Select last tab
$('#myTab li:eq(2) a').tab('show') // Select third tab (0-indexed)

#### Markup
You can activate a tab or pill navigation without writing any JavaScript by simply specifying data-toggle="tab" or data-toggle="pill" on an element. Adding the nav and nav-tabs classes to the tab ul will apply the Bootstrap tab styling, while adding the nav and nav-pills classes will apply pill styling.

<div role="tabpanel">

  <!-- Nav tabs -->
  <ul class="nav nav-tabs" role="tablist">
    <li role="presentation" class="active"><a href="#home" aria-controls="home" role="tab" data-toggle="tab">Home</a></li>
    <li role="presentation"><a href="#profile" aria-controls="profile" role="tab" data-toggle="tab">Profile</a></li>
    <li role="presentation"><a href="#messages" aria-controls="messages" role="tab" data-toggle="tab">Messages</a></li>
    <li role="presentation"><a href="#settings" aria-controls="settings" role="tab" data-toggle="tab">Settings</a></li>
  </ul>

  <!-- Tab panes -->
  <div class="tab-content">
    <div role="tabpanel" class="tab-pane active" id="home">...</div>
    <div role="tabpanel" class="tab-pane" id="profile">...</div>
    <div role="tabpanel" class="tab-pane" id="messages">...</div>
    <div role="tabpanel" class="tab-pane" id="settings">...</div>
  </div>

</div>

#### Fade effect
To make tabs fade in, add .fade to each .tab-pane. The first tab pane must also have .in to properly fade in initial content.

<div class="tab-content">
  <div role="tabpanel" class="tab-pane fade in active" id="home">...</div>
  <div role="tabpanel" class="tab-pane fade" id="profile">...</div>
  <div role="tabpanel" class="tab-pane fade" id="messages">...</div>
  <div role="tabpanel" class="tab-pane fade" id="settings">...</div>
</div>

#### Methods

##### $().tab

Activates a tab element and content container. Tab should have either a data-target or an href targeting a container node in the DOM.

<ul class="nav nav-tabs" role="tablist" id="myTab">
  <li role="presentation" class="active"><a href="#home" aria-controls="home" role="tab" data-toggle="tab">Home</a></li>
  <li role="presentation"><a href="#profile" aria-controls="profile" role="tab" data-toggle="tab">Profile</a></li>
  <li role="presentation"><a href="#messages" aria-controls="messages" role="tab" data-toggle="tab">Messages</a></li>
  <li role="presentation"><a href="#settings" aria-controls="settings" role="tab" data-toggle="tab">Settings</a></li>
</ul>

<div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="home">...</div>
  <div role="tabpanel" class="tab-pane" id="profile">...</div>
  <div role="tabpanel" class="tab-pane" id="messages">...</div>
  <div role="tabpanel" class="tab-pane" id="settings">...</div>
</div>

<script>
  $(function () {
    $('#myTab a:last').tab('show')
  })
</script>

#### Events

When showing a new tab, the events fire in the following order:

hide.bs.tab (on the current active tab)
show.bs.tab (on the to-be-shown tab)
hidden.bs.tab (on the previous active tab, the same one as for the hide.bs.tab event)
shown.bs.tab (on the newly-active just-shown tab, the same one as for the show.bs.tab event)
If no tab was already active, then the hide.bs.tab and hidden.bs.tab events will not be fired.

Event Type	Description
show.bs.tab	This event fires on tab show, but before the new tab has been shown. Use event.target and event.relatedTarget to target the active tab and the previous active tab (if available) respectively.
shown.bs.tab	This event fires on tab show after a tab has been shown. Use event.target and event.relatedTarget to target the active tab and the previous active tab (if available) respectively.
hide.bs.tab	This event fires when a new tab is to be shown (and thus the previous active tab is to be hidden). Use event.target and event.relatedTarget to target the current active tab and the new soon-to-be-active tab, respectively.
hidden.bs.tab	This event fires after a new tab is shown (and thus the previous active tab is hidden). Use event.target and event.relatedTarget to target the previous active tab and the new active tab, respectively.
Copy
$('a[data-toggle="tab"]').on('shown.bs.tab', function (e) {
  e.target // newly activated tab
  e.relatedTarget // previous active tab
})


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
