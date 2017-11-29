---
layout: docs
title: To Do
group: jcu
---

This is a *living style guide* and as such will always be a work-in-progress.
If you have suggestions, please get in touch.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}


## Known Issues

* No automatically aligned dropdown menus within the viewport:
  <https://github.com/twbs/bootstrap/issues/17167>
* Accordion example in docs uses old v3 Panels:
  <https://github.com/twbs/bootstrap/pull/17159>
* abbr double-underline in Firefox:
  <https://github.com/twbs/bootstrap/issues/16574>
* Print grid columns: <https://github.com/twbs/bootstrap/issues/16800>

## To Do List

* Decide on version numbering to distinguish / relate Bootstrap to the JCU web
  framework

* Store 'approved' brand images and supporting resources in a Git repository
  (ask Digital Media team)

* Build process:

  * Minification for CSS actually produces a *larger* file than originally
    provided.

  * Run base templates and CSS styles through WCAG2AAA / Section508 checker or
    linter

  * Accessibility:

    * Ensure ARIA labels and standards are met by *all* examples.

  * Workflow for removing certain components from the framework.  Perhaps just a
    have a bare-bones "JCU" framework for just the core components.

## To resolve

* Best tool for managing external dependencies (Bower, Grunt, Gulp, Npm...)
* Ensure there's a distinction between an application and the CMS.  Have to
  clearly highlight which application it is in some manner.
* Test across browsers
* Accessibility standards

