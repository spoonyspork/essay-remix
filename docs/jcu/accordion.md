---
layout: docs
title: Accordion
group: jcu
---

This is a customisation of the standard Bootstrap
[Collapse]({{ site.baseurl }}/components/collapse) component from its core, integrating
brand-specific colours and animations.  Refer to the main documentation for full
documentation and other types of collapsible components.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Example

{% example html %}
<div class="jcu-accordion" role="tablist" aria-multiselectable="true">
  <div class="card">
    <div class="card-header" id="headingOne" role="tab">
      <a class="jcu-accordion__toggle" data-toggle="collapse" href="#collapseOne" role="button" aria-expanded="true" aria-controls="collapseOne">
        Heading
      </a>
    </div>
    <div class="collapse in" id="collapseOne" role="tabpanel" aria-labelledby="headingOne">
      <div class="card-block">
        Some text
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="headingTwo" role="tab">
      <a class="jcu-accordion__toggle collapsed" data-toggle="collapse" href="#collapseTwo" role="button" aria-expanded="true" aria-controls="collapseOne">
        Heading2
      </a>
    </div>
    <div class="collapse" id="collapseTwo" role="tabpanel" aria-labelledby="headingTwo">
      <div class="card-block">
        Some text
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="headingThree" role="tab">
      <a class="jcu-accordion__toggle collapsed" data-toggle="collapse" href="#collapseThree" role="button" aria-expanded="true" aria-controls="collapseThree">
        Heading3
      </a>
    </div>
    <div class="collapse" id="collapseThree" role="tabpanel" aria-labelledby="headingThree">
      <div class="card-block">
        Some text
      </div>
    </div>
  </div>
</div>
{% endexample %}
