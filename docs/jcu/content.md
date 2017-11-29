---
layout: docs
title: JCU Content
group: jcu
---

*Content* is a specific JCU component for the display and representation of
the main section of information on a given page.  This is typically centric on
details that are to be displayed to users, rather than to be interactive.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}


## Examples

### Standard

Define a *Content* element with `.jcu-content` and add anything you'd like to into
it:

{% example html %}
<div class="jcu-content">
  <p class="lead text-primary">
    One of the world's leading institutions focusing on the tropics,
    Australia's James Cook University is surrounded by the spectacular ecosystems of
    the rainforests of the Wet tropics, the dry savannahs, and the iconic <a
    href="#">Great Barrier Reef</a>.
  </p>
  <h2>Born for the tropics</h2>
  <p>
    Ranked in the <a href="https://www.jcu.edu.au/world-rankings">top four
    percent</a> of the world's tertiary institutions by the respected Academic
    Ranking of World Universities produced by the Shanghai Jiao Tong University,
    James Cook University is dedicated to creating a brighter future for life in the
    tropics world-wide, through graduates and discoveries that make a
    difference.
  </p>
</div>
{% endexample %}

### Short Content

If you're working on a page with a very short amount of content, and displaying
an Exposition, you may need the *Content* component to cover a certain minimum
height such that the final page looks correct.  To achieve this, add
`.jcu-content--short-content`:

{% example html %}
<div class="jcu-content jcu-content--short-content">
  <p>This is just one line of content.</p>
</div>
{% endexample %}

### Printing

*Content* will automatically add the URL after any links within the content during
printing.  For any absolute URLs (such as `https://jcu.io/web`), they will be
written to the printed page as is.  For any relative URLs (such as
`/web/framework.html` or `../framework.html`), they will be written as-is.
Root-relative URLs can be prefixed for easier understanding by using CSS code
such as this, adjusting the prefix to fit your system:

{% highlight css %}
.jcu-content a[href^="/"]::after {
  content: " (https://www.jcu.edu.au" attr(href) ") ";
}
{% endhighlight %}

