---
layout: page
title: Buttons
---

Buttons are used for **actions**, like in forms, while textual hyperlinks are used for **destinations**, or moving from one page to another.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Default buttons

Use the standard—yet classy—`.btn` for form actions and primary page actions. These are used extensively around the site.

When using a `<button>` element, **always specify a `type`**. When using a `<a>` element, **always add `role="button"` for accessibility**.

{% example html %}
<button class="btn" type="button">Button button</button>
<a class="btn" href="#" role="button">Link button</a>
{% endexample %}

You can find them in two sizes: the default `.btn` and the smaller `.btn-sm`.

{% example html %}
<button class="btn" type="button">Button</button>
<button class="btn btn-sm" type="button">Small button</button>
{% endexample %}

## Primary

Primary buttons are green and are used to indicate the *primary* action on a page. When you need your buttons to stand out, use `.btn.btn-primary`. You can use it with both button sizes—just add `.btn-primary`.

{% example html %}
<button class="btn btn-primary" type="button">Primary button</button>
<button class="btn btn-sm btn-primary" type="button">Small primary button</button>
{% endexample %}

## Danger

Danger buttons are red. They help reiterate that the intended action is important or potentially dangerous (e.g., deleting a repo or transferring ownership). Similar to the primary buttons, just add `.btn-danger`.

{% example html %}
<button class="btn btn-danger" type="button">Danger button</button>
<button class="btn btn-sm btn-danger" type="button">Small danger button</button>
{% endexample %}

## Outline

Outline buttons downplay an action as they appear like boxy links. Just add `.btn-outline` and go.

{% example html %}
<button class="btn btn-outline" type="button">Outline button</button>
<button class="btn btn-sm btn-outline" type="button">Outline button</button>
{% endexample %}

## Action

Action buttons are a little fancier than Outline buttons. Just add `.btn-action`.

{% example html %}
<button class="btn btn-action" type="button">Action button</button>
<button class="btn btn-sm btn-action" type="button">Action button</button>
{% endexample %} 

## Link

Link buttons take up the same amount of space as buttons, but have no outlines. Great for lining up a primary and secondary action.

{% example html %}
<button class="btn btn-primary" type="button">Primary button</button>
<button class="btn btn-link" type="button">Link button</button>
{% endexample %}


## Disabled state

Disable `<button>` elements with the boolean `disabled` attribute and `<a>` elements with the `.disabled` class.

{% example html %}
<button class="btn" type="button" disabled>Disabled button</button>
<a class="btn disabled" href="#" role="button">Disabled button</a>
{% endexample %}

Similar styles are applied to primary, danger, outline and action buttons:

{% example html %}
<button class="btn btn-primary" type="button" disabled>Disabled button</button>
<a class="btn btn-primary disabled" href="#" role="button">Disabled button</a>
{% endexample %}

{% example html %}
<button class="btn btn-danger" type="button" disabled>Disabled button</button>
<a class="btn btn-danger disabled" href="#" role="button">Disabled button</a>
{% endexample %}

{% example html %}
<button class="btn btn-outline" type="button" disabled>Disabled button</button>
<a class="btn btn-outline disabled" href="#" role="button">Disabled button</a>
{% endexample %}

{% example html %}
<button class="btn btn-action" type="button" disabled>Disabled button</button>
<a class="btn btn-action disabled" href="#" role="button">Disabled button</a>
{% endexample %}

## Block buttons

Make any button full-width by adding `.btn-block`. It adds `width: 100%;`, changes the `display` from `inline-block` to `block`, and centers the button text.

{% example html %}
<p><button class="btn btn-block" type="button">Block button</button></p>
<p><button class="btn btn-sm btn-block" type="button">Small block button</button></p>
{% endexample %}

## With counts

You can easily append a count to a **small button**. Add the `.with-count` class to the `.btn-sm` and then add the `.social-count` after the button.

**Be sure to clear the float added by the additional class.**

{% example html %}
<div class="clearfix">
  <a class="btn btn-sm btn-with-count" href="#" role="button">
    <span class="ki-eye"></span>
    Watch
  </a>
  <a class="social-count" href="#">6</a>
</div>
{% endexample %}

You can also use the [counter](utilities/#counter) component within buttons:

{% example html %}
<button class="btn" type="button">
  Button
  <span class="counter">12</span>
</button>

<button class="btn btn-primary" type="button">
  Button
  <span class="counter">12</span>
</button>

<button class="btn btn-danger" type="button">
  Button
  <span class="counter">12</span>
</button>

<button class="btn btn-outline" type="button">
  Button
  <span class="counter">12</span>
</button>
{% endexample %}

## Button groups

Have a hankering for a series of buttons that are attached to one another? Wrap them in a `.btn-group` and the buttons will be rounded and spaced automatically.

{% example html %}
<div class="btn-group">
  <button class="btn" type="button">Button</button>
  <button class="btn" type="button">Button</button>
  <button class="btn" type="button">Button</button>
</div>

<div class="btn-group">
  <button class="btn btn-outline" type="button">Button</button>
  <button class="btn btn-outline" type="button">Button</button>
  <button class="btn btn-outline" type="button">Button</button>
</div>

<div class="btn-group">
  <button class="btn btn-sm" type="button">Button</button>
  <button class="btn btn-sm" type="button">Button</button>
  <button class="btn btn-sm" type="button">Button</button>
</div>
{% endexample %}

Add `.button_to` to `<form>`s within `.btn-group`s for proper spacing and rounded corners.

**Heads up!** This class name is inconsistent and will change in the next major version.

{% example html %}
<div class="btn-group">
  <form class="button_to">
    <button class="btn" type="button">Button in a form</button>
  </form>
  <button class="btn" type="button">Button</button>
  <button class="btn" type="button">Button</button>
</div>
{% endexample %}

## Javascript Buttons

Do more with buttons. Control button states or create groups of buttons for more components like toolbars.

<div class="flash flash-error">
  <strong>Cross-browser compatibility</strong>
  Firefox persists form control states (disabledness and checkedness) across page loads. A workaround for this is to use autocomplete="off". See Mozilla bug #654072.
</div>

### Stateful

Add `data-loading-text="Loading..."` to use a loading state on a button.

<div class="flash" style="margin-bottom: 1rem">
  <strong>Use whichever state you like!</strong>
  For the sake of this demonstration, we are using `data-loading-text` and `$().button('loading')`, but that's not the only state you can use. See more on this below in the `$().button(string)` documentation.
</div>

{% example html %}
<button type="button" id="myButton" data-loading-text="Loading" class="btn btn-primary" autocomplete="off">
  Press for a loading state
</button>

<script>
  $('#myButton').on('click', function () {
    var $btn = $(this)
    $btn.button('loading'),
    setTimeout(function() {
      $btn.button('reset')
    }, 3e3)
  })
</script>
{% endexample %}

### Single toggle

Add `data-toggle="button"` to activate toggling on a single button.

<div class="flash flash-error" style="margin-bottom: 1rem">
  <strong>Pre-toggled buttons need <code>.active</code> and <code>aria-pressed="true"</code>.</strong>
  For pre-toggled buttons, you must add the <code>.active</code> class and the <code>aria-pressed="true"</code> attribute to the button yourself.
</div>

{% example html %}
<button type="button" class="btn" data-toggle="button" aria-pressed="false" autocomplete="off">
  Single toggle
</button>
{% endexample %}

### Checkbox / Radio

Add `data-toggle="buttons"` to a `.btn-group` containing checkbox or radio inputs to enable toggling in their respective styles.

<div class="flash flash-error" style="margin-bottom: 1rem">
  <strong>Preselected options need <code>.active</code></strong>
  For preselected options, you must add the <code>.active</code> class to the input's label yourself.
</div>

<div class="flash flash-error" style="margin-bottom: 1rem">
  <strong>Visual checked state only updated on click</strong>
  If the checked state of a checkbox button is updated without firing a <code>click</code> event on the button (e.g. via <code>&lt;input type="reset"></code> or via setting the <code>checked</code> property of the input), you will need to toggle the <code>.active</code> class on the input's label yourself.
</div>

{% example html %}
<div class="btn-group" data-toggle="buttons">
  <label class="btn active">
    <input type="checkbox" autocomplete="off" checked> Checkbox 1 (pre-checked)
  </label>
  <label class="btn">
    <input type="checkbox" autocomplete="off"> Checkbox 2
  </label>
  <label class="btn">
    <input type="checkbox" autocomplete="off"> Checkbox 3
  </label>
</div>
{% endexample %}

{% example html %}
<div class="btn-group" data-toggle="buttons">
  <label class="btn active">
    <input type="radio" name="options" id="option1" autocomplete="off" checked> Radio 1 (preselected)
  </label>
  <label class="btn">
    <input type="radio" name="options" id="option2" autocomplete="off"> Radio 2
  </label>
  <label class="btn">
    <input type="radio" name="options" id="option3" autocomplete="off"> Radio 3
  </label>
</div>
{% endexample %}

### Methods

#### $().button('toggle')

Toggles push state. Gives the button the appearance that it has been activated.

#### $().button('reset')

Resets button state - swaps text to original text.

#### $().button(string)

Swaps text to any data defined text state.

{% highlight html %}
<button type="button" id="myStateButton" data-complete-text="finished!" class="btn btn-primary" autocomplete="off">
  ...
</button>

<script>
  $('#myStateButton').on('click', function () {
    $(this).button('complete') // button text will be "finished!"
  })
</script>
{% endhighlight %}
