---
layout: docs
title: Coding Guide
group: jcu
---

{% callout info %}
**Heads up!** You probably don't need this if you're an application owner or
developer and not part of the Web or Marketing teams. However, you might like to
try and keep your application (especially if it's a custom or in-house one) up
to the standards set by this framework.
{% endcallout %}

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Tools

* [W3C default element ARIA semantics](http://www.w3.org/TR/html5/dom.html#ariusage-notea)
* [W3C Nu HTML checker](https://validator.w3.org/nu/)

## Recommended practices

### New technologies

* Use [Can I use](http://caniuse.com) to determine if a browser feature is
  widely available across user agents and what, if any, workarounds are
  available or caveats should be noted.

### Accessibility

All templates must be accessible and pass standards Section 508 and WCAG2AA.
In order to test accessibility, we use a number of different tools:

* [pa11y](http://pa11y.org): command-line and server driven testing of
  rendered pages using a local browser instance.  This uses the HTML5
  CodeSniffer and is capable of Section508 and WCAG2 testing.

* [tota11y](https://khan.github.io/tota11y/): in-browser testing of elements
  within actual pages.  Follow the instructions on the project page to use
  `tota11y` on live application or any other pages. `tota11y` is also included
  on all documentation pages for additional testing—look for the glasses in the
  bottom-left corner!

  Use `tota11y` to determine contrast ratios for absolutely positioned
  elements where `pa11y` reports warnings.

For how to use these tools in practice, see
[Accessibility testing]({{ site.baseurl }}/jcu/building/#accessibility-testing).

### Coding guide

* Follow the [Code Guide](http://codeguide.co) HTML and CSS standards; these
  guidelines are what Bootstrap strives to abide by.  In terms of specific class
  names, follow BEM (Block, Element, Modifier) semantic syntax, where possible.

  * Note that BEM only applies if styling is DOM-dependent, for instance a
    heading or list that is styled *because* it is within another class.

* Use only CSS classes for selectors in styling; do not use IDs.  Note that this
  only applies to styling and does not apply JavaScript-based components that
  require IDs for operation.

* All components are given names that describe their purpose, rather than being
  arbitrary or specifically dictating their position.  This also has the added
  benefit of making components easily identifiable and discussable.  For
  example, the [Exposition]({{ site.baseurl }}/jcu/exposition)
  component sets the theme for the page with a background image and the
  [Explorer]({{ site.baseurl }}/jcu/explorer) component consists of
  the way in which users can navigate and *explore* a content-rich site.

* All custom variables and classes in code should follow Bootstrap's lead
  and use American English (for example, ``color`` over ``colour``).  This
  decision is for consistency when mixing stock and custom variables.  Comments
  and content in documentation pages should follow standard Australian English
  spelling and grammar (``colour``).

* Avoid all use of inline styles within the framework; reusable classes should
  be provided instead.

* Consistently name files: [suggestion coming]

* Internet Explorer's print layouts for A4 adhere to `sm` (small) sized media
  queries.  In order to combat this, ensure print layouts are not affected or
  are specifically excluded in `@include media-breakpoint-down` styles.
