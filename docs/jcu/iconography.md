---
layout: docs
title: Iconography
group: jcu
---

Iconography is provided care of the [WebHostingHub
Glyphs](http://www.webhostinghub.com/glyphs/) and full details can be found on
their official documentation.

{% callout warning %}
**Heads up!** There are potential issues that arise with using an icon font.
Take a read of [Seriously, Don't Use Icon
Fonts](http://blog.cloudfour.com/seriously-dont-use-icon-fonts/).  We may
adapt our use towards SVGs in the near future.
{% endcallout %}

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Examples

Icons should be specified using a `<span>` element, in the manner shown.  Other
examples in some documentation may use an `<i>` element but JCU systems should
use `<span>` where possible for consistency and accessibility (some testers show
screen readers interpret the latter as readable).

### Reference

<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="../../dist/css/components/webhostinghub-glyphs/demo.html"></iframe>
</div>

[View the reference]({{ site.baseurl
}}/dist/css/components/webhostinghub-glyphs/demo.html){:target="_blank"} (opens
in new window)

{% callout warning %}
**Heads up!** There are some minor differences in icon naming from the original
official version of WebHostingHub Glyphs.  Once example that JCU is using on the
CMS website is `.icon-emailalt` for an envelope icon; this is called
`.icon-email2` in the framework's version.
{% endcallout %}

### Decorative

Icons that are *purely* decorative and add no meaning can be hidden from
accessibility devices.

{% example html %}
<span class="icon-asterisk" aria-hidden="true"></span>
<span class="icon-plus" aria-hidden="true"></span>
<span class="icon-cloud" aria-hidden="true"></span>
<span class="icon-edit" aria-hidden="true"></span>
<span class="icon-wineglass" aria-hidden="true"></span>
<span class="icon-grid" aria-hidden="true"></span>
{% endexample %}

### Semantic

Icons that convey meaning on the page should be labelled accordingly.  Think of
`aria-label` like `title` or `alt` for `img` tags.

In this example, the icons are being used in place of the name of the social
media service and need to be labelled to aid accessibility.

{% example html %}
<a href="https://www.facebook.com/jamescookuniversity"><span class="sr-only">Facebook</span><span class="icon-circlefacebook" aria-label="Facebook icon"></span></a>
<a href="https://twitter.com/jcu"><span class="sr-only">Twitter</span><span class="icon-circletwitter" aria-label="Twitter icon"></span></a>
<a href="https://www.youtube.com/jamescookuniversity"><span class="sr-only">YouTube</span><span class="icon-youtube" aria-label="YouTube icon"></span></a>
<a href="https://plus.google.com/+jamescookuniversity"><span class="sr-only">Google+</span><span class="icon-circlegoogleplus" aria-label="Google+ icon"></span></a>
{% endexample %}
