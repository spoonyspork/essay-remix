---
layout: docs
title: Toolbar
group: jcu
---

*Toolbar* is a is the top-level navigation bar that is fixed to the top of all
CMS-style pages.

Its primary purpose is to provide links and menus linking to
the key JCU systems, but can be re-purposed in other types of internal systems.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

### Worked example

See the [Content Page example]({{ site.baseurl }}/examples/jcu-content-page/)
for a fully-worked, living example. The toolbar uses the YAMM (Yet Another
Megamenu) Bootstrap add-on to allow grid layouts within the dropdown menus.

### Basic example

{% example html %}
<nav class="jcu-toolbar navbar navbar-fixed-top navbar-dark bg-inverse">
  <div class="container-fluid">
    <div class="row">
      <ul class="nav navbar-nav">
        <li class="nav-item dropdown dropdown--open-on-hover">
          <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Students</a>
          <div class="dropdown-menu" role="menu">
            <div class=".h1">Dropdown contents go here</div>
          </div>
        </li>
        <li class="nav-item dropdown dropdown--open-on-hover">
          <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Staff</a>
          <div class="dropdown-menu" role="menu">
            <div class=".h1">Dropdown contents go here</div>
          </div>
        </li>
        <li class="nav-item"><a class="nav-link" href="#">Alumni</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Library</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Maps</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Contacts</a></li>
      </ul>
    </div>
  </div>
</nav>
{% endexample %}
