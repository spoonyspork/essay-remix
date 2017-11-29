---
layout: docs
title: Download
group: jcu
---

The framework can be downloaded or accessed in a number of different ways depending
on the type of application being themed.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## CDN-hosted resources

You can utilise our Content Distribution Network (CDN)-hosted resources to
style your web application or site and avoid needing to download anything.

### CSS & JS

{% highlight html %}
  <link rel="stylesheet" href="{{ site.cdn.css }}" integrity="{{ site.cdn.css_hash }}" crossorigin="anonymous">
  <script src="{{ site.cdn.js }}" integrity="{{ site.cdn.js_hash }}" crossorigin="anonymous"></script>
{% endhighlight %}

Upgrading to a new release version is a matter of updating the included URLs
and following any applicable [Migration]({{ site.baseurl }}/migration/)
documentation.

If using the JavaScript resources above, ensure you have jQuery and Tether
available on your page.  If your page or application doesn't already have
them, you can also load these using CDN as well, via the following:

{% highlight html %}
  <script src="{{ site.cdn.jquery }}" integrity="{{ site.cdn.jquery_hash }}" crossorigin="anonymous"></script>
  <script src="{{ site.cdn.tether }}" integrity="{{ site.cdn.tether_hash }}" crossorigin="anonymous"></script>
{% endhighlight %}

### Images and other resources

It is also possible to reference any of the images or other content located on
the CDN as well, like so:

{% example html %}
<img src="{{ site.cdn.base}}/images/jcua-logo-campus-stack-full-colour.svg">
{% endexample %}

Relative paths refer to the content located in the `dist/` directory. You can
determine the path to content on the CDN by viewing
<{{ site.repo }}/tree/master/dist>.

## Release packages

<a class="btn btn-outline-primary" href="{{ site.download.dist }}">Download
latest release</a>
<a class="btn btn-outline-primary" href="{{ site.download.releases }}">See all
versions</a>

Releases are simply fully compiled zip archives, containing all the necessary
files and resources to implement the JCU Web Framework in your project.  This is
best suited for:

* Static web pages
* Small to medium sites
* Systems without Git available
* Developers unfamiliar with Git

To apply to your site or system, see the
[Quick Start]({{ site.baseurl }}/jcu/introduction/#quick-start) documentation.

To update to a new version of the framework, remove the old version and unzip
the new version in the same area.  Check the [Migration]({{ site.baseurl
}}/migration/) notes first regarding what has changed and how your system needs to
adapt.  As with all systems, ensure you have backups and test in a development
environment first.

## From Git

### Releases from Git

<a class="btn btn-outline-primary" href="{{ site.repo }}">Access repository</a>

Applications can track the framework's releases through Git, a common
distributed version control system (DVCS).  This has the added benefit of simply
being able to pull changes and checkout new versions and avoid manually handling
files.

This is best suited for:

* Larger websites or projects
* Systems with Git installed
* Projects using Git for version control

If your project is already using Git for version control, you can add
the framework as a [Git
submodule](http://www.git-scm.com/book/en/Git-Tools-Submodules), which will
assist with managing updates.

To apply to your site or system, consult the [Application Theming]({{
site.baseurl }}/jcu/application-theming) documentation.  As different platforms
work in different ways, we encourage you to submit your experiences as a pull
request (or open an issue and we'll help).

### Source files

<a class="btn btn-outline-primary" href="{{ site.baseurl }}/jcu/building/">Let's get building!</a>

Download the complete project, including all source files for Sass, JavaScript
and documentation.  If you want to create your own flavour of framework, choose
just specific parts, or do something else that's a little out there, you're in
the right place.

This is best suited for:

* Projects with specific styling requirements
* Customising and tweaking the final theme
* Selecting and reusing specific components
* Users with experience with npm, Sass, Grunt and front-end build tools
* Projects using Git for version control

To get started building, consult the documentation for
[Building]({{ site.baseurl }}/jcu/building/) for step-by-step instructions.
