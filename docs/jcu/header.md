---
layout: docs
title: Content
group: jcu
---

*Header* is a specific JCU component for the display and representation of
the upper portion of a given page or layout.  This is typically centric on
branding, navigation, and titular details.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

{% callout info %}
**Heads up!** The examples are defined using the `<header>` element which
implies the ARIA role of `banner`. Consider adjusting the element to `<div>` or
otherwise if you want the display of a Header but want to avoid the semantics
imposed.
{% endcallout %}

### Standard

Define a *Header* element with `.jcu-header` and add anything you'd like to into
it:

{% example html %}
<header class="container jcu-header">
  <div class="row">
    <div class="col-xs-12">
      <h1 class="jcu-header__page-title">ResearchOnline@JCU</h1>
    </div>
  </div>
</header>
{% endexample %}

### Banner

A *banner* style header is primarily utilitarian in that it presents the brand
and clearly identifies the page or site.  On larger displays, the banner will
add a top margin and padding.

This example shows adding a background image for additional context or vibrancy
to a given site or page.

{% example html %}
<header class="container jcu-header jcu-header--banner jcu-bg--blue-fish">
  <div class="row jcu-bg--black-50pc">
    <div class="col-xs-6">
      <a class="jcu-brand" href="https://www.jcu.edu.au">
        <img class="img-fluid" src="{{ site.baseurl }}/dist/images/jcua-logo-mono-reversed.svg" alt="JCU Australia logo">
      </a>
    </div>
    <div class="col-xs-6 text-xs-right">
      <h1 class="jcu-header__page-title" id="page-title2"><a href="#">Site title</a></h1>
    </div>
  </div>
</header>
{% endexample %}

### Marketing

The *marketing* style header is utilised for content of such a nature - general
information that users would utilise to form their opinion of our brand.

TODO: add details
