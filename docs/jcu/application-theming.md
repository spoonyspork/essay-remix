---
layout: docs
title: Application Theming
group: jcu
---

Different applications require different approaches to making them consistent
with the rest of the University's online presence.

If you have completed the theming of an application, we'd like to feature your
notes here. Get in touch or send a pull request with your changes.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Approaches

### CDN-hosted resources <span class="label label-success">Easiest</span>

If you're just looking to include a release version of the JCU Web Framework
in your app or pages, use our Content Distribution Network (CDN)-hosted
resources and avoid needing to download anything.  This approach involves
placing suitable HTML tags into your page and that's it.  If you want to use
resources like images and logos from the CDN, you can do that as well just by
linking to appropriate resource.

<a class="btn btn-outline-primary" href="{{ site.baseurl
}}/jcu/download/#cdn-hosted-resources">Learn how to use our CDN</a>


### Static sites or editable source <span class="label label-info">Easy-Medium</span>

Your application was created in-house or you otherwise have full control over the
underlying source code (such as Coldfusion apps or the Research Portfolio), then
it's a matter of customising the application to suit.  The general guide is to:

1. Include the JCU Web Framework resources in your page following one of the
   options on the [Download]({{ site.baseurl }}/jcu/download/) page.

1. Customise the source of your application to be Bootstrap-compatible.  For
   instance, `<button>` elements become `<button class="btn">` and so
   forth.

1. Follow the documentation you're currently reading until all aspects of your
   application are adjusted or themed accordingly.

You can also make use of any [examples]({{ site.baseurl }}/examples/) provided
as base templates.

To update to a newer version of the JCU Web Framework, replace the framework
files and follow any instructions in the [Migration documentation]({{ site.baseurl }}/migration/).

{% callout info %}
If you're working with static files and trying things locally, note that
Firefox does not allow relative includes for font-face in CSS.  This means
that fonts and iconography is unlikely to load.  See the [relevant
bug](https://bugzilla.mozilla.org/show_bug.cgi?id=760436) for details.

Use `about:config` to change `security.fileuri.strict_origin_policy`
temporarily to `false` to relax this restriction and reload your page.
{% endcallout %}


### Open source <span class="label label-info">Easy-Medium</span>

If the application you're working with is open source, then you will be able to
modify its implementation to suit.  Since Bootstrap is a very common web
front-end framework, you will likely find that your application either has
native support for Bootstrap markup or a community-developed theme or templates
available.  The general guide, if Bootstrap is used, is to:

1. Locate how the application is serving its resources.

1. Customise them to feature the JCU Web Framework instead of stock Bootstrap
   resources.

1. Adjust the application's templates and remaining code to fit the JCU web
   framework; leverage the example templates given.

   Follow the instructions in [Editable source](#editable-source) for
   more information.

### Vendor-hosted <span class="label label-warning">Medium-Hard</span>

If your application is hosted by a vendor, refer to your application
documentation for information on what theming customisations are possible.

In general, you want to ask your vendor for:

* Technologies being used
* Whether modifying HTML output is possible
* Any templating or theming documentation
* How to serve web resources (CSS, JavaScript, images, fonts)

Once you have these details in hand, you can make a well-informed decision about
the easiest way forward.  If your application is hosted, but is actually
open source (such as a Wordpress blog), then you may have more success than a
remotely-hosted, closed source product.

### Closed source <span class="label label-danger">Hard</span>

Closed source applications are entirely dependent on the software developer or
vendor for features and support.  Consult your application and developer to
determine whether it has the ability to be themed and what this extends to.

In applications where theming options are otherwise limited, you may only be
able customise specific colours, logos, or so forth, rather than underlying HTML
templates.  In this case, use your best judgement to reach a compromise that
looks as close to JCU as possible.  Resources such as images can be obtained
from a JCU Web Framework release package.

Another option may be to implement a middleware technology (such as XSLT or
an XSLT wrapper such as [Diazo](http://diazo.org)) on top of your application
and to transform the HTML on-the-fly.
