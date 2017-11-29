---
layout: docs
title: Section Navigator
group: jcu
---

*Section Navigator* is an amalgam of a navbar, consisting of the current
site or section's navigation, and breadcrumbs.  This is typically used
CMS-style pages.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

### Worked example

See the [Content Page example]({{ site.baseurl }}/examples/jcu-content-page/)
for a fully-worked, living example.

### Basic example

<style type="text/css">
.jcu-section-navigator {
  margin-top: 0;
}
</style>

{% example html %}
<div class="jcu-section-navigator">
  <div class="container-fluid hidden-print">
    <nav class="navbar navbar-dark bg-inverse">
      <ul class="nav navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="#">About JCU</a>
        </li>
        <li class="nav-item dropdown dropdown--open-on-hover">
          <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Campuses</a>

          <div class="dropdown-menu" role="menu">
            <a class="dropdown-item" href="#" role="menuitem">Townsville</a>
            <a class="dropdown-item" href="#" role="menuitem">Cairns</a>
            <a class="dropdown-item" href="#" role="menuitem">Singapore</a>
            <a class="dropdown-item" href="#" role="menuitem">Brisbane</a>
            <a class="dropdown-item" href="#" role="menuitem">Mackay</a>
            <a class="dropdown-item" href="#" role="menuitem">Mount Isa</a>
            <a class="dropdown-item" href="#" role="menuitem">Thursday Island</a>
          </div>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">History</a>
        </li>
      </ul>
    </nav>
  </div>
  <div class="container-fluid jcu-section-navigator__breadcrumb">
    <nav class="breadcrumb" aria-label="Breadcrumbs">
      <a class="breadcrumb-item" href="#">About JCU</a>
      <a class="breadcrumb-item" href="#">History and Information</a>
      <span class="breadcrumb-item active">About</span>
    </nav>
  </div>
</div>
{% endexample %}
