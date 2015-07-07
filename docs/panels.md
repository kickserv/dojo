---
layout: page
title: Panels
---

Dojo panels should be used to separate logical sections of Kickserv content.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Panel Structure

Panels must follow a structure as indicated below.

{% example html %}
<div class="panel">
  <div class="panel-header">
    <div class="panel-content">
      <h3 class="panel-title">Using Dojo be like...</h3>
    </div>
  </div>
  <div class="panel-body">
    <div class="panel-content text-center">
      <img src="http://gifs.joelglovier.com/gangsta/42-Snoop-Bounce.gif" />
    </div>
  </div>
  <div class="panel-footer">
    <div class="panel-content">
      <div class="form-actions">
        <button type="button" class="btn btn-primary">Save changes</button>
        <button type="button" class="btn">Cancel</button>
      </div>
    </div>
  </div>
</div>
{% endexample %}

## With Sidebar

In many cases, it may be necessary to include content in a toggleable sidebar. Note the nesting of the `.panel-sidebar`.

**Note:** Sidebars are hidden by default. Add `.show` to show the sidebar.

{% example html %}
<div class="panel">
  <div class="panel-header">
    <div class="panel-content">
      <a href="#sidebar" class="right js-toggle">
        Show Sidebar
        <i class="ki-settings icon-right"></i>
      </a>
      <h3 class="panel-title">How does the sidebar work?</h3>
    </div>
  </div>
  <div class="panel-body-with-sidebar">
    <div class="panel-body">
      <div class="panel-content text-center">
        <img src="http://gifs.joelglovier.com/mind-blown/magic.gif" />
      </div>
    </div>
    <div class="panel-sidebar show" id="sidebar">
      <div class="panel-content">
        This sidebar area will grow to accommodate your content. Make sure you set a max-width when necessary.
      </div>
    </div>
  </div>
</div>
{% endexample %}

You can use a script like this to create a toggle for the sidebar.

{% highlight javascript %}
$('.js-toggle').on("click", function() {
  var target = $(this).attr('href');
  $(target).toggleClass('show');
});
{% endhighlight %}

## With Tables

Use the following structure to contain a table in a panel. Note the use of `.panel-table` in place of `.panel-content`.

{% highlight html %}
<div class="panel">
  <div class="panel-header">
    <div class="panel-content">
      <h3 class="panel-title">How does the sidebar work?</h3>
    </div>
  </div>
  <div class="panel-body">
    <div class="panel-table">
      <table class="table">
        ...
      </table>
    </div>
  </div>
</div>
{% endhighlight %}
