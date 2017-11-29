---
layout: docs
title: Styling for JCU
group: jcu
---

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Where from?

The styles in this web front-end framework are a mixture of those provided by
the original Squiz CMS layouts, [JCU Brand
Manual](https://www.jcu.edu.au/marketing-toolkit), and Bootstrap's original
designs.  This documentation, forked from the original Bootstrap project,
illustrates all available styles for use within projects associated with JCU.

In a number of circumstances, the Squiz CMS layouts use browser defaults (such
as font sizes, weights, spacing, margins and so forth).  Defaults from Firefox
(version 43) have been used to fill this gap and ensure the theme remains
consistent across browsers.

## Inclusions

* Webhostinghub-Glyphs
* OpenSans font
* jQuery

## Theming an application

See [Application
Theming]({{ site.baseurl }}/jcu/application-theming) for
details on how to apply these styles to your own projects.

## Extending or reusing

For projects with additional requirements, this framework can be extended in the
same way that Bootstrap itself can.  The original base SCSS files can be
included in an extension project and customised further.

Given the complexity and variations between applications, especially those that
are vendor-supplied, we expect that all projects will require some degree of
customisation.  If you have suggestions for customisations that should feature
as part of this core framework, contact the web and marketing team, or create an
issue at {{ site.repo }}.

## Decisions and theory

* Semantic markup is used where possible to for aspects such as header and
  footer, groups of links with headings (`nav` + `h1`), and logical section
  groupings.  It may look like a `<h1>` is out of place in some examples, but
  the sectioning ensures the context is correct.

* Multi-level dropdown menus were removed from Bootstrap for usability reasons
  and this remains the case for this framework.  In cases where multi-level
  menus might feel required, try simplifying the situation and thinking of
  another way to get people to the pages or actions you want them to do.

* Squiz uses its CMS metadata fields to control background images and colours on
  pages.  These then are translated into either inline styles on a rendered page.
  From a structural point-of-view, this isn't a sustainable practice, as styles
  aren't centrally controlled.  In order to simplify this, all repeatable
  aspects, such as Overlays, are defined in the main style sheet files.  This
  makes for consistency across all systems using the framework, and eliminates a
  potential maintenance burden from application owners.

