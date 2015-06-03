---
layout: page
title: Navbar
---

Dojo comes with a navbar custom-designed for Kickserv.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Main Navbar

The main navbar contains the Kickserv logo, main app sections, and account menu.

{% example html %}
<div class="grid-block shrink navbar">
  <div class="grid-block shrink">
    <div class="grid-content ks-logo text-center">
      <a href="/">
        <%= image_tag "connect/nav_icon.svg", class: "ks-logo", alt: "Connect", height: "54" %>
      </a>
    </div>
  </div>
  <div class="grid-block" id="ks-nav">
    <div class="grid-content ks-nav">
      <ul class="ks-nav-blocks">
        <% if labs?(:portal_2) %>
          <li class="active">
            <%= link_to conversations_path(anchor: "/messages") do %>
              <i class="octicon octicon-comment-discussion"></i>
              <span class="ks-nav-label">Messages</span>
            <% end %>
          </li>
        <% end %>
        <li>
          <%= link_to opportunities_path do %>
            <i class="octicon octicon-clippy"></i>
            <span class="ks-nav-label">Estimates</span>
          <% end %>
        </li>
        <li>
          <%= link_to schedule_path do %>
            <i class="octicon octicon-briefcase"></i>
            <span class="ks-nav-label">Jobs</span>
          <% end %>
        </li>
        <li>
          <%= link_to customers_path do %>
            <i class="octicon octicon-file-text"></i>
            <span class="ks-nav-label">Invoices</span>
          <% end %>
        </li>
        <li>
          <%= link_to customers_path do %>
            <i class="octicon octicon-organization"></i>
            <span class="ks-nav-label">Contacts</span>
          <% end %>
        </li>
      </ul>
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
</div>

{% endexample %}

## Subnav

On certain pages, it may be necessary to include a subnav bar. Use the following structure and include as necessary.

{% example html %}
<div class="subnav">
  <div class="grid-block">
    <div class="grid-content">
      <ul class="ks-nav-pills">
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
