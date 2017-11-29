---
layout: docs
title: Exposition
group: jcu
---

*Exposition* sets the tone and describes the content or intent of the given page
or site through background imagery.  It is designed to sit behind all other
content on a page and typically used on a CMS-style pages.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

### Worked example

See the [Content Page example]({{ site.baseurl }}/examples/jcu-content-page/)
for a fully-worked, living example.

## Basic demonstration

This is a simple example of how this component can express the topic area and
theme of the page.  By default, *Exposition* is positioned behind all other
elements on a page using a negative *z-index*.

<style type="text/css">
/* Workarounds for z-index not showing in examples */
.bd-example .jcu-exposition {
  z-index: 0;
}
.bd-example {
  overflow: hidden;
}
</style>

<div class="bd-example">
  <div class="jcu-exposition hidden-print">
    <img src="{{ site.baseurl }}/dist/images/backgrounds/GreenLeafSwirl.jpg" alt="Leaf curl image" role="presentation">
  </div>
  <div class="jcu-content col-xs-6 col-xs-offset-3">
    <h1>This text sits atop the Exposition</h1>
    <p>This is content.</p>
  </div>
</div>

{% highlight html %}
<div class="jcu-exposition hidden-print">
  <img src="{{ site.baseurl }}/dist/images/backgrounds/GreenLeafSwirl.jpg" alt="Leaf curl image" role="presentation">
</div>
<div class="jcu-content">
  <h1>This text sits atop the Exposition</h1>
  <p>This is content.</p>
</div>
{% endhighlight %}
