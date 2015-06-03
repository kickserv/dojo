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
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!--[if lt IE 7 ] <html lang="#{current_account.locale}" class="no-js ie6">-->
<!--[if IE 7 ] <html lang="#{current_account.locale}" class="no-js ie7">-->
<!--[if IE 8 ] <html lang="#{current_account.locale}" class="no-js ie8">-->
<!--[if IE 9 ] <html lang="#{current_account.locale}" class="no-js ie9">-->
<!-- [if (gt IE 9)|!(IE)]><!-->
<html class="no-js" lang="<%= current_account.locale %>">
  <!-- <![endif]-->
  <head>
    <meta charset="utf-8"/>
    <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible"/>
    <title>
      <%= page_title %>
      <%= "(#{Rails.env}:#{commit_sha})" unless Rails.env.production? || Rails.env.beta? %>
    </title>
    <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
    <%= favicon_link_tag '/favicon.ico' %>
    <%= csrf_meta_tag %>
    <!-- Le HTML5 shim, for IE6-8 support of HTML5 elements-->
    <!--[if lt IE 9]--><script src="//html5shim.googlecode.com/svn/trunk/html5.js"></script><!-- <![endif]-->
    <%= yield :before_app_style %>
    <link href="//netdna.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css" rel="stylesheet">
    <%= stylesheet_link_tag "ks-app", :media => "screen, print" %>
    <%= yield(:head) %>
  </head>

  <body class="ks-app <%= @body_class %>" data-class_group="Application">
    <%= render partial: "shared/gtm" %>
    <div class="grid-frame">
      <%= render 'layouts/masquerading' if masquerading? %>
      <%= render partial: "layouts/nav_ks_app" %>
      <div class="grid-block vertical">
        <%= yield(:subnav) %>
        <%= ks_flash_div *(flash.keys - [ :logged_in ]) %>
        <div class="grid-block ks-content-block">
          <%= yield %>
        </div>
      </div>
    </div>

    <%= render :partial => "layouts/js_ssk_preferences" %>
    <%= yield :modal %>
    <%= render :partial => 'layouts/delete_confirmation' %>
    <%= render :partial => 'layouts/generic_lightbox' %>
    <%= render :partial => 'layouts/signature_modal' %>
    <%= render :partial => 'layouts/mark_job_complete_modal' %>

    <%= javascript_include_tag "application" %>
    <%= javascript_include_tag "https://maps.googleapis.com/maps/api/js?key=#{ENV['MAP_KEY']}&sensor=false" %>
    <%= yield :javascript %>

    <script>
      $(document).ready(function() {
        $('.js-flash-close').on('click', function() {
          $(this).parents('.ks-flash-messages').remove()
        })

        $('.js-dropdown-toggle').on("click", function() {
          var target = $(this).attr('href');
          $(target).toggleClass('show');
        });

        $(document).click(function (e) {
          var current_target = $(e.target);
          if (!current_target.closest(".js-dropdown").length && !current_target.closest(".js-dropdown-toggle").length) {
            $('.js-dropdown').removeClass('show');
          }

        });

        $('.js-sidebar-toggle').on("click", function() {
          var target = $(this).attr('href');
          $(target).toggleClass('show');
        });

      })
    </script>

    <% unless masquerading? && Rails.env.production? %>
      <%= intercom_script_tag %>
    <% end %>
  </body>
</html>
{% endhighlight %}
