---
layout: docs
title: Colophon
group: jcu
---

*Colophon*, as it is in publishing, is a way of conveying the publication
date and time and copyright information about current resource.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

{% callout info %}
**Heads up!** Examples provided in templates may use `<section>` rather than
`<div>` for semantic reasons. Use an appropriate HTML5 section element to suit
your application and structure.
{% endcallout %}

### With publishing date

Suitable for use on CMS or other content-centric pages that require the
publishing date to be shown.

{% example html %}
<div class="jcu-colophon">
  <ul class="list-inline">
    <li class="list-inline-item">Published Sunday, 20 Sep 2015 15:00</li>
    <li class="list-inline-item">Copyright &copy; 1995 to 2015 James Cook University.  All rights reserved.</li>
    <li class="list-inline-item">ABN 46253211955</li>
  </ul>
</div>
{% endexample %}

### Without publishing date

This suits dynamic applications and other situations whereby a publication date
is inapplicable or inappropriate.

{% example html %}
<div class="jcu-colophon">
  <ul class="list-inline">
    <li class="list-inline-item">Copyright &copy; 1995 to 2015 James Cook University.  All rights reserved.</li>
    <li class="list-inline-item">ABN 46253211955</li>
  </ul>
</div>
{% endexample %}
