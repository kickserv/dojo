---
layout: page
title: Modals
---

Dojo modals should be used to accomplish tasks that *must* be completed before a user can continue.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Modal Structure

Modals must follow a structure as indicated below.

{% highlight html %}
<div class="modal fade">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span class="octicon octicon-x"></span></button>
        <h4 class="modal-title">Modal title</h4>
      </div>
      <div class="modal-body">
        <p>One fine body&hellip;</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
{% endhighlight %}

## Demo Modal


{% example html %}
<button type="button" class="btn btn-primary " data-toggle="modal" data-target="#example_modal">
  Launch demo modal
</button>

<div class="modal fade" id="example_modal">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span class="octicon octicon-x"></span></button>
        <h4 class="modal-title">Modal title</h4>
      </div>
      <div class="modal-body">
        <p>One fine body&hellip;</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
{% endexample %}

## Optional Sizes

{% example html %}
<!-- Large modal -->
<button type="button" class="btn btn-primary" data-toggle="modal" data-target=".bs-example-modal-lg">Large modal</button>

<div class="modal fade bs-example-modal-lg" tabindex="-1" role="dialog" aria-labelledby="myLargeModalLabel" aria-hidden="true">
  <div class="modal-dialog modal-lg">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span class="octicon octicon-x"></span></button>
        <h4 class="modal-title">Large modal</h4>
      </div>
      <div class="modal-body">
        <p>&hellip;</p>
      </div>
    </div>
  </div>
</div>

<!-- Small modal -->
<button type="button" class="btn btn-primary" data-toggle="modal" data-target=".bs-example-modal-sm">Small modal</button>

<div class="modal fade bs-example-modal-sm" tabindex="-1" role="dialog" aria-labelledby="mySmallModalLabel" aria-hidden="true">
  <div class="modal-dialog modal-sm">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span class="octicon octicon-x"></span></button>
        <h4 class="modal-title">Small modal</h4>
      </div>
      <div class="modal-body">
        <p>&hellip;</p>
      </div>
    </div>
  </div>
</div>
{% endexample %}
