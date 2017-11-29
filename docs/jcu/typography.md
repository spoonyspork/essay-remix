---
layout: docs
title: Typography customisations
group: jcu
---

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

### Text

{% example html %}
<div class="bg-inverse text-inverse">
  <p>.text-inverse inverts text for dark backgrounds</p>
</div>
{% endexample %}

{% example html %}
<div class="row">
  <div class="col-xs-3">
    <button class="btn btn-primary text-wrap">.text-wrap forces wrapping, especially on buttons</button>
  </div>
</div>
{% endexample %}

### Blocks

{% example html %}
<div class="block--dotted">
  <h3>Contact details</h3>
  <p>To RSVP, please visit <a href="http://web.jcu.io">http://web.jcu.io</a>.</p>
  <p>For further information, please contact <a href="mailto:example@jcu.edu.au">example@jcu.edu.au</a>.</p>
</div>
{% endexample %}

### Bordered List (inside borders)

A border is present between each list item, and not present on the first or last
item in a list.  This is extended to create the [Campus
Stack]({{ site.baseurl }}/jcu/campus-stack).

{% example html %}
<ul class="list-bordered">
  <li>How do I apply at JCU?</li>
  <li>Where can I get support on campus?</li>
  <li>What is a supplementary exam?</li>
</ul>
{% endexample %}

The border reflects the width of the list block, rather than the content:

{% example html %}
<div class="row">
  <div class="col-xs-4">
    <ul class="list-bordered">
      <li>How do I apply at JCU?</li>
      <li>Where can I get support on campus?</li>
      <li>What is a supplementary exam?</li>
    </ul>
  </div>
</div>
{% endexample %}
