---
layout: docs
title: Dropdowns
group: jcu
---

These are minor customisations that can be applied to Bootstrap's
[Dropdowns]({{ site.baseurl }}/components/dropdowns) to achieve various outcomes.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

### YAMM

[YAMM (Yet Another Megamenu)](https://github.com/geedmo/yamm3) for Bootstrap is
a small add-on to the Bootstrap framework that adds the ability to use the
standard grid layout without dropdown menus.

For the most up-to-date examples, consult the [official YAMM
documentation](https://geedmo.github.io/yamm3/).

See the [Content Page example]({{ site.baseurl }}/examples/jcu-content-page/)
for a fully-worked, living example in the context of this framework; the
Students and Staff dropdown menus use YAMM.

### Open on Hover

Add the `.dropdown--open-on-hover` class to any given `.dropdown` element and
its dropdown menu will open on hover rather than click.  This also absolves the
element from needing a ID on the element marked with the ``.dropdown-toggle``
class and from needing to specify any ``data-*`` attributes at all.

{% callout warning %}
Use this sparingly because users expect that they can interact explicitly with
page components, such as dropdowns, rather than having interaction happen
automatically. See [Bootstrap explained:
Dropdowns](http://markdotto.com/2012/02/27/bootstrap-explained-dropdowns/) for
more information.
{% endcallout %}

Compare the two:

{% example html %}
<div class="btn-group">
  <div class="btn-group">
    <div class="dropdown dropdown--open-on-hover">
      <a class="btn btn-secondary dropdown-toggle" id="dropdownmenu-button1" data-target="dropdown" aria-haspopup="true" aria-expanded="false">JCU Campuses (hover)</a>
      <div class="dropdown-menu" role="menu" aria-labelledby="dropdownmenu-button1">
        <a class="dropdown-item" href="#" role="menuitem">Townsville</a>
        <a class="dropdown-item" href="#" role="menuitem">Cairns</a>
        <a class="dropdown-item" href="#" role="menuitem">Singapore</a>
      </div>
    </div>
  </div>

  <div class="btn-group">
    <div class="dropdown">
      <a class="btn btn-secondary dropdown-toggle" id="dropdownmenu-button2" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">JCU Campuses (click)</a>
      <div class="dropdown-menu" role="menu" aria-labelledby="dropdownmenu-button2">
        <a class="dropdown-item" href="#" role="menuitem">Townsville</a>
        <a class="dropdown-item" href="#" role="menuitem">Cairns</a>
        <a class="dropdown-item" href="#" role="menuitem">Singapore</a>
      </div>
    </div>
  </div>
</div>
{% endexample %}

