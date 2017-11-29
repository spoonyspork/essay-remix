---
layout: docs
title: Layout
group: jcu
---

In order to achieve the page layouts and designs, the framework implements
several additional layout aspects.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

### Print grid layout

* `.col-pr-12` forces a grid layout container to using `100%` width when
  printed. This is the only print grid layout class provided as a simple
  shortcut.  If fully-featured printing is required consult [issue
  #15042](https://github.com/twbs/bootstrap/issues/15042) or
  [#16800](https://github.com/twbs/bootstrap/issues/16800).

### Maximum-width fluid container

This differs from a nested `.container` and `.container-fluid` approach as that
results in just a fixed-width container at different breakpoints.  This is a
fluid container that possesses a specific maximum width.

{% example html %}
<div class="container-fluid container-fluid--max-width">
  <p>This container is fluid, but only until the max-width limit.  You probably
  won't see any effect in this example.</p>
</div>
{% endexample %}


### Flexbox

[Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout),
or the Flexible Box Layout Module, is a method of positioning elements
in horizontal or vertical stacks.  This positioning module resolves many issues
around floating elements, absolute positioning and scripting hacks to achieve
its results.  Browser support is [steadily
increasing](http://caniuse.com/#search=flexbox), and in most cases, degrades
reasonably well into older browsers.

These convenience classes allow easy alignment of content, particularly within
the grid system:

{% example html %}
<div class="row flex-items-start">
  <div class="col-xs-4 jcu-bg--black"><h1>Aligned</h1></div>
  <div class="col-xs-4 jcu-bg--blue"><h3>to the</h3></div>
  <div class="col-xs-4 jcu-bg--green"><h6>top</h6></div>
</div>
{% endexample %}

{% example html %}
<div class="row flex-items-center">
  <div class="col-xs-4 jcu-bg--black"><h1>Containers</h1></div>
  <div class="col-xs-4 jcu-bg--blue"><h3>are vertically</h3></div>
  <div class="col-xs-4 jcu-bg--green"><h6>centred</h6></div>
</div>
{% endexample %}

{% example html %}
<div class="row flex-items-end">
  <div class="col-xs-4 jcu-bg--black"><h1>Algined</h1></div>
  <div class="col-xs-4 jcu-bg--blue"><h3>to the</h3></div>
  <div class="col-xs-4 jcu-bg--green"><h6>bottom</h6></div>
</div>
{% endexample %}

### Flexbox and print

* `.visible-print-flex` provides a useful class to hide an element from display
  on a screen, but set its display to be `flex` on print.  This is essentially
  the same as `.visible-print-block` from Bootstrap core, just for Flexbox
  instead.
