---
layout: page
title: Tables
---

Tables should be used to display data like Events, Jobs, or Contacts.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc} 

## Structure

Tables should follow the following HTML structure.

{% highlight html %}
<table class="table">
  <thead>
    <tr>
      <th>A heading</th>
      <th>Another heading</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Footer content</td>
      <td>Yes, it belongs here in the markup</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Some cell content</td>
      <td>Some more</td>
    </tr>
  </tbody>
</table>
{% endhighlight %}

**Note:** The `tfoot` actually belongs immediately following the `thead`. This is to facilitate loading of the head and foot content before a potentially length `tbody`.

## Table Input

For an input that uses the entire cell for a click target, use the following html. *This works best for radio buttons and checkboxes, but could theoretically be used for any input type.*

{% example html %}
<table class="table">
  <thead>
    <tr>
      <th class="table-input">
        <label><input type="checkbox" /></label>
      </th>
      <th>Name</th>
      <th>Email Address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="table-input">
        <label><input type="checkbox" /></label>
      </td>
      <td>Norman the Ninja</td>
      <td>norman@kickserv.com</td>
    </tr>
  </tbody>
</table>
{% endexample %}

## Table Action

For a link that uses the entire cell for a click target, use the following html. These can only be used in the `tbody` or `tfoot`.

{% example html %}
<table class="table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Email Address</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Norman the Ninja</td>
      <td>norman@kickserv.com</td>
      <td class="table-action">
        <a href="">
          <i class="ki-megaphone"> </i>
        </a>
      </td>
    </tr>
  </tbody>
</table>
{% endexample %}

### Danger Table Action

For potentially dangerous table actions, use `.table-action-danger` in addition. These can only be used in the `tbody` or `tfoot`.

{% example html %}
<table class="table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Email Address</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Norman the Ninja</td>
      <td>norman@kickserv.com</td>
      <td class="table-action table-action-danger">
        <a href="">
          <i class="ki-trashcan"> </i>
        </a>
      </td>
    </tr>
  </tbody>
</table>
{% endexample %}

## With Blankslates

If no data is available to display in a table, use a blankslate. *Note the use of the wrapper class on the table cell.*

**Note:** Always use the `.clean-background` version inside a table.

{% example html %}
<table class="table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Email Address</th>
      <th>Phone Number</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="3" class="with-blankslate">
        <div class="blankslate spacious clean-background">
          <span class="mega-ki-broadcast"></span>
          <h3>Nothing to see here...</h3>
          <p><a href="">Add a new contact</a>, or why not kick back and relax?</p>
        </div>
      </td>
    </tr>
  </tbody>
</table>
{% endexample %}
