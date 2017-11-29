---
layout: docs
title: Themes
group: jcu
---

*Themes* are overarching colour schemes which can be applied to content on sites
or pages.  Themes currently only apply to headings, but may be expanded to
influence other aspects of colour across a page at a later time.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

{% callout info %}
The given classes, such as `.jcu-theme--blue`, can be applied at any level of
your document to influence the styling contents.  If you experience issues with
specificity, you can apply (or re-apply the class) at a more specific element on
your page.
{% endcallout %}

`.h1` through `.h6` classes are also available for when you want to match the
colour and styling of a heading but still want your text to be displayed
inline or otherwise retain the same semantics relating to its HTML.

{% example html %}
<div class="jcu-theme--blue">
  <h1>h1. Heading</h1>
  <h2>h2. Heading</h2>
  <h3>h3. Heading</h3>
  <h4>h4. Heading</h4>
  <h5>h5. Heading</h5>
  <h6>h6. Heading</h6>
  <hr>
  <p>
    <span class="h1">.h1 class</span>
    <span class="h2">.h2 class</span>
    <span class="h3">.h3 class</span>
    <span class="h4">.h4 class</span>
    <span class="h5">.h5 class</span>
    <span class="h6">.h6 class</span>
  </p>
</div>
{% endexample %}

{% example html %}
<div class="jcu-theme--orange">
  <h1>h1. Heading</h1>
  <h2>h2. Heading</h2>
  <h3>h3. Heading</h3>
  <h4>h4. Heading</h4>
  <h5>h5. Heading</h5>
  <h6>h6. Heading</h6>
  <hr>
  <p>
    <span class="h1">.h1 class</span>
    <span class="h2">.h2 class</span>
    <span class="h3">.h3 class</span>
    <span class="h4">.h4 class</span>
    <span class="h5">.h5 class</span>
    <span class="h6">.h6 class</span>
  </p>
</div>
{% endexample %}

{% example html %}
<div class="jcu-theme--green">
  <h1>h1. Heading</h1>
  <h2>h2. Heading</h2>
  <h3>h3. Heading</h3>
  <h4>h4. Heading</h4>
  <h5>h5. Heading</h5>
  <h6>h6. Heading</h6>
  <hr>
  <p>
    <span class="h1">.h1 class</span>
    <span class="h2">.h2 class</span>
    <span class="h3">.h3 class</span>
    <span class="h4">.h4 class</span>
    <span class="h5">.h5 class</span>
    <span class="h6">.h6 class</span>
  </p>
</div>
{% endexample %}

{% example html %}
<div class="jcu-theme--red">
  <h1>h1. Heading</h1>
  <h2>h2. Heading</h2>
  <h3>h3. Heading</h3>
  <h4>h4. Heading</h4>
  <h5>h5. Heading</h5>
  <h6>h6. Heading</h6>
  <hr>
  <p>
    <span class="h1">.h1 class</span>
    <span class="h2">.h2 class</span>
    <span class="h3">.h3 class</span>
    <span class="h4">.h4 class</span>
    <span class="h5">.h5 class</span>
    <span class="h6">.h6 class</span>
  </p>
</div>
{% endexample %}
