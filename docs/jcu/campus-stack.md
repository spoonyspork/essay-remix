---
layout: docs
title: Campus Stack
group: jcu
---

*Campus Stack* is a simple component for visually listing the JCU campuses,
and is featured in the Brand Manual.  Its primary purpose is to feature in the
footer of the main website, but can be re-used if necessary.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

{% callout info %}
Any of the following examples can be scaled using CSS.  For example, to make a
small campus stack, you can utilise the built-in `.small` class attached to the
list tag.
{% endcallout %}

### Mono

The standard, mono-coloured stack:

{% example html %}
<ul class="jcu-campus-stack">
  <li><a href="#">Cairns</a></li>
  <li><a href="#">Singapore</a></li>
  <li><a href="#">Townsville</a></li>
</ul>
{% endexample %}

### Colour

The colour stack:

{% example html %}
<ul class="jcu-campus-stack jcu-campus-stack--color">
  <li><a href="#">Cairns</a></li>
  <li><a href="#">Singapore</a></li>
  <li><a href="#">Townsville</a></li>
</ul>
{% endexample %}

### Inverse

The inverted stack, for use on coloured backgrounds:

<div class="bd-example jcu-bg--gradient-blue">
  <ul class="jcu-campus-stack jcu-campus-stack--inverse">
    <li><a href="#">Cairns</a></li>
    <li><a href="#">Singapore</a></li>
    <li><a href="#">Townsville</a></li>
  </ul>
</div>

{% highlight html %}
<ul class="jcu-campus-stack jcu-campus-stack--inverse">
  <li><a href="#">Cairns</a></li>
  <li><a href="#">Singapore</a></li>
  <li><a href="#">Townsville</a></li>
</ul>
{% endhighlight %}
