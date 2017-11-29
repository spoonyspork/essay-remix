---
layout: docs
title: Introduction
group: jcu
redirect_from: "/jcu/"
---

This is the web front-end framework for James Cook University and is used
by various web applications at JCU.  The JCU Web Framework builds upon
[Bootstrap](http://getbootstrap.com), a popular framework for building
responsive, mobile-first sites and applications.

This *living style guide* features reusable components for web applications and 
provides a starting point for theming JCU projects on the web.  The
documentation features worked examples of:

* All Bootstrap standard components
* Demonstrations of styles fitting in with JCU's branding guides
* Customised components, including brand imagery
* Third party libraries (iconography, fonts)
* Interactive page templates

No two web applications are identical and how an application owner or vendor
themes an app will also.  Bootstrap was selected as the base for this project as
its ubiquitous nature means that software products and vendors are likely to
already have a theming story involving Bootstrap, if they don't already use
Bootstrap by default.

Here's how to quickly get started with the assets and a template starter page.

## Quick start

In this quick start, we'll focus on the fundamentals of including the assets in
a static HTML page.

{% callout info %}
**Heads up!** Various [download options]({{ site.baseurl }}/jcu/download), including
cloning from Git, are available too.
{% endcallout %}

1. Download the [latest release zip]({{ site.download.dist }}), taking note of
   the version used.

2. Unzip the files.

3. Copy-paste the stylesheet `<link>` into your `<head>` to load our CSS.
   It is recommended that you place this before all other stylesheets.

   ~~~ html
   <link rel="stylesheet" href="css/jcu.min.css">
   ~~~

4. Ensure that your site or application has jQuery available. Consult the
   [JavaScript]({{ site.baseurl}}/getting-started/javascript) documentation to
   determine which versions are compatible.

5. Add the web framework JavaScript plugins near the end of your pages, right before
   the closing `</body>` tag. Be sure to place jQuery first as Bootstrap code
   depends on it:

   ~~~ html
   <script src="js/jcu.min.js"></script>
   ~~~

And that's it — you're on your way to a fully Bootstrapped site. If you're
unsure about the general page structure, see the main [Bootstrap
Introduction]({{ site.baseurl }}/getting-started/introduction/#starter-tempate)
for an example page template.

Your application is probably more complex, but the fundamentals remain
the same: you need to serve the framework's assets (CSS, JavaScript, images,
fonts) and add these to your pages.

<a class="btn btn-outline-primary" href="{{ site.baseurl }}/jcu/application-theming">Learn about application theming</a>
