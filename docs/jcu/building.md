---
layout: docs
title: Building
group: jcu
---

{% callout info %}
**Heads up!** You don't need to read this documentation if you're just looking
to use a pre-produced version.  If you're looking to extend or customise the JCU
Web Framework further then read on.
{% endcallout %}

{% callout warning %}
**First things first!** If you haven't read the documentation on Bootstrap's
[Build tools]({{ site.baseurl }}/getting-started/build-tools), head over there
and go through that first.  Everything here will make a lot more sense once you
also understand the purpose of each tool Bootstrap uses and that you have those
tools installed on your system.
{% endcallout %}

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Getting started

How you get started depends on your operating system.  The simplest
option is to use a terminal and if you are on a Mac or Linux computer, you'll
have the required tools already present by default -- a Terminal and the ``git``
command.  If you're on Windows, or otherwise looking for a GUI solution, you'll
need to install some form Git application (such as [GitHub
Desktop](https://desktop.github.com/)) to help you manage the code.

1. This project uses [EditorConfig](http://editorconfig.org/) to maintain
   consistent styling for indenting and line endings.  Ensure your editor of
   choice is configured with support for EditorConfig; there are many
   [plugins](http://editorconfig.org/#download) available.

1. Visit the [web framework repository]({{ site.repo }}) repository and clone
   it.  You'll find clone URLs at the top-left side of the page.  Ensure that
   you clone the repository *recursively*, which ensures that third-party
   submodules are also obtained.  For those using a terminal, run:

   ~~~ shell
   git clone --recursive {{ site.repo }}
   ~~~

1. Ensure all of the
   [Build tools]({{ site.baseurl }}/getting-started/build-tools) needed
   are installed on your system.

1. Install any Node.js dependencies with:

   ~~~ shell
   cd jcu-web-framework
   npm install
   ~~~

   <a name="a11y-install"></a>Optionally, if you'd like to carry out
   accessibility testing, install these additional tools (noting that
   administrative or `sudo` access may be required):

   ~~~ shell
   npm install -g pa11y phantomjs
   ~~~

1. Your system may already have a Ruby environment configured. As such, it is
   easier and cleaner to have Bundler install its resources locally to the
   `jcu-web-framework` directory with:

   ~~~ shell
   bundler install --path vendor/bundle
   ~~~

   Once you've run this once, you don't need to specify the path if you re-run
   `bundle`.  If just run `bundle` or `bundle install`, Bundler will try and
   install the required gems in your system path.

1. Now you're ready to build and test!

## Grunt tasks

All tasks from the default Bootstrap
[Gruntfile]({{ site.baseurl }}/getting-started/build-tools#using-grunt) are
automatically available.  Our Gruntfile adds the following commands and tasks:

| Task | Description |
| --- | --- |
| `grunt jcu-publish` | Builds documentation via Jekyll for hosting, and uploads to the `gh-pages` branch in the repo. |
| `grunt jcu-cdn` | Push the current dist release to the CDN hosting using Rsync. |
| `grunt dist-images` | `grunt dist-images` optimises images in the `/images` directory, placing the results in `/dist/images`. This is incorporated as part of `grunt dist` and doesn't need to be run directly.  **Uses [grunt-image](https://github.com/1000ch/grunt-image), which uses various image optimisers under the hood.** |

## Branches and structure

* Latest stable version is always located in `master` branch
* Development changes take place on the `develop` branch
* Features and developments should branch off `develop`
* Fixes can be made via pull request to the `develop` branch
* Releases are tagged using SemVer (for example, `v4.0.0`)

This branching model follows that of
[Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow),
following Bootstrap's lead for version numbers.

## Making changes

1. Make changes to the repository and save your files with your favourite
   editor.  Ensure that your editor is compatible with EditorConfig to ensure
   that file formats and line endings are correct and stay that way.

1. Test and build the framework (`dist`) and the documentation (`docs`):

   ~~~ shell
   grunt dist docs
   ~~~

   Once you've done this the first time, you can run:

   ~~~ shell
   grunt watch
   ~~~

   to continue watching for further changes.  This is a lot faster than having
   to re-run the above commands manually and particularly helpful if
   you're trying out a few different changes at once.

1. Build and serve the documentation:

   ~~~ shell
   bundler exec jekyll serve
   ~~~

1. Load and inspect the documentation at <http://localhost:9001> in your browser.
   There are a number of JCU customisation pages, which you must add to or
   expand if you are adding a new web component.  There are a number of example
   layouts which are used by downstream web applications for theming; you can use
   these for testing your changes.

{% callout info %}
If you're doing a lot of work, you can leave the two latter commands above
running simultaneously (in different terminals) as you make changes.  They'll
automatically detect all changes to the main SCSS files and documentation and
rebuild everything automagically.
{% endcallout %}

## Accessibility testing

### tota11y

To test with `tota11y`, the in-browser visualisation toolkit, use the glasses
icon at the bottom-left of any documentation page or custom JCU examples. For
any non-JCU examples, install and use the Bookmarklet, available on the [tota11y
project page](https://khan.github.io/tota11y/#Installation).

Click the glasses now and see how you can toggle heading markers, colour
contrast, link text testing, and more.

{% callout info %}
`pa11y`, with its Section508 and WCAG2 tests, is limited in its ability to test
absolutely positioned elements within a web page and produces warnings to this
effect (`Warning: This element is absolutely positioned and the background color
can not be determined [...]`).  `tota11y` should be used in these situations to
test via its `Contrast` toggle.
{% endcallout %}

### pa11y

`pa11y` is a command-line tool that can be used to test pages against Section508
and WCAG2. For an in-depth introduction, consule [Accessibility Testing with
pa11y](http://cruft.io/posts/accessibility-testing-with-pa11y/).

To test the framework's pages:

1. Ensure that you've followed the instructions for [Getting
   started](#getting-started) and that you have installed the [accessibility
   tools](#a11y-install).

1. Start a documentation server running with:

   ~~~ shell
   bundler exec jekyll serve
   ~~~

1. In another terminal, test individual pages, one at a time, with:

   ~~~ shell
   pa11y <url>
   pa11y --standard Section508 <url>
   ~~~

   If not specified, the `--standard` defaults to `WCAG2AA`.

   So, to test the Content Page example:

   ~~~ shell
   pa11y http://localhost:9001/examples/jcu-content-page
   pa11y --standard Section508 http://localhost:9001/examples/jcu-content-page
   ~~~

1. Consult the report and follow its suggestions to improve and fix the given
   page structure or corresponding CSS.

1. When complete, commit the results to the framework.


## Updating Bootstrap versions

The JCU Web Framework is built upon Bootstrap and adds a number of *commits*
which change various settings, add new features and generally craft Bootstrap
into a framework that's in-keeping with JCU's branding guide.  There will come
times when the underlying version of Bootstrap should be upgraded to either
introduce new features, fix bugs, or perhaps stay up-to-date with the latest web
practices and standards.

Because we are using Git to track versions, the commands to run this
process are straightforward.  Resolving differences between JCU's customisations
and Bootstrap core requires careful attention as Bootstrap may restructure or
otherwise can change significantly between versions.

1. Add the official Bootstrap repository as a remote called `upstream` in your
   cloned repository and fetch its contents.  For those using a terminal, run:

   ~~~ shell
   cd jcu-web-framework
   git remote add upstream https://github.com/twbs/bootstrap.git
   git fetch --no-tags upstream
   ~~~

1. Fetch the latest changes from the `upstream` remote.  In a terminal, this is:

   ~~~ shell
   git fetch --no-tags upstream
   ~~~

1. Determine the version you wish to update to and attempt the merge,
   substituting in your version number:

   ~~~ shell
   git merge v4.1.1
   ~~~

   The merge can be specified as anything that Git recognises as a reference; in
   this case, we use a tag for a specific version, but can, if the need arises,
   be a branch name or commit hash.

1. You will likely be informed that merge conflicts have occurred.  These appear
   where the changes in JCU's framework are at odds with changes in the official
   Bootstrap code.

   Go through each file (except those in `dist/` or `docs/dist/`) that is
   conflicted and resolve the merge.  See [this
   page](https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/)
   from GitHub on how to resolve conflicts on the command line.  Your Git
   application likely offers similar functionality.  In essence, you'll edit
   each conflicted file, merge changes together, and stage (`git add …`) the
   files.

   For any files located in `dist/` or `docs/dist`, you can leave these until
   rebuilding the framework as they are generated from the `grunt` build tasks
   you'll run in the next step.

1. Once all non `dist/` and `docs/dist` conflicts are resolved, build and test
   the framework.

   1. You *must* re-run the installation steps in order to update any
      dependencies for changes between Bootstrap versions:

      ~~~ shell
      npm install
      bundle
      ~~~

   1. Now build the framework. Most technical issues (such as changes to
      variable names and classes) will show at this point.

      ~~~ shell
      grunt dist docs
      ~~~

      If you're continuing to work on the framework, use `grunt watch` to
      automatically rebuild on changes.

   1. Visually inspect and test the components and documentation via your web
      browser.  Start a documentation server with:

      ~~~ shell
      bundler exec jekyll serve
      ~~~

      and load <http://localhost:9001> in your browser.  Visual and accessibility
      issues need to be inspected by loading the examples and style guide in your
      browser to ensure things appear correctly.  To resolve issues, ensure you
      check:

      * [Official migration documentation]({{ site.baseurl }}/migration)
      * `git blame` or Git version control history for the upstream repository
      * Existing classes being renamed or extended (such as `text-right` to
        `test-[size]-right`)
      * Core variables that have been added or adjusted (such as
        `$font-size-base` to `16px` )
      * Modification to existing classes or structure (such as addition of extra
        padding to `.dropdown-menu`)

1. Once fully tested, make a note in the change log (`CHANGELOG.md`), commit
   the results and push to the server.

1. Rebuild the main documentation, push to the server and deploy to CDN in one
   go by running:

   ~~~ shell
   grunt prep-release jcu-publish
   ~~~

   If this happens to complain about uncommitted changes in the working
   directory, even if there are none.  In this case, you can run the final commit
   task manually:

   ~~~ shell
   grunt buildcontrol:pages
   ~~~

## Updating third-party components

The JCU Web Framework is built upon several extra components that underpin
certain aspects such as the dropdown menus and icons.  These are all held within
the `scss/components` directory and managed as [Git
submodules](https://www.git-scm.com/book/en/v2/Git-Tools-Submodules).

Firstly, in order to update one of these components, determine the version to
update to as a Git reference (such as a branch name, tag or commit).  You'll use
this to `checkout` in the process that follows.  These instructions are for
those using a terminal; adapt them to your own environment.

1. Change into the component directory:

   ~~~ shell
   cd scss/components/[component-id]
   ~~~

1. Fetch the latest changes for this submodule's repository:

   ~~~ shell
   git fetch
   ~~~

1. Checkout the version you wish to update to that you determined earlier.

   ~~~ shell
   git checkout [version-id]
   ~~~

1. Change back to the main framework directory and pull any nested submodule
   updates:

   ~~~ shell
   cd ../../..
   git submodule update --init --recursive
   ~~~

1. Commit the change in component version into the main framework:

   ~~~ shell
   git commit scss/components/[component-id]
   ~~~

   Ensure that you add a suitable commit message explaining what the change was
   and what effect it has.

It is rare that these components will need to be updated, though bug fixes and
new features will need to be drawn in from time to time.

## Releasing a new JCU Web Framework version

* Complete testing, commit all existing changes and run the final build for
  this new version with:
  ``grunt dist docs``

* Commit any final changes from this command and ensure you are in a clean Git checkout.

* Run `node grunt/change-version.js [old-version] [new-version]` at the root
  of the repository. Do not include `v` in the version numbering.  This will
  change all versions across all different files, including JS, CSS, package
  files and documentation.

* Follow instructions from [SRIHash.org](https://www.srihash.org/) to generate
  an SRI hash of the production minified versions of CSS and JS:

      openssl dgst -sha384 -binary dist/css/jcu.min.css | openssl base64 -A
      openssl dgst -sha384 -binary dist/js/jcu.min.js | openssl base64 -A

* Change the documentation `_config.yml` to reflect these SRI changes and
  rebuild the documentation with:

      grunt docs

* Commit the results of the version change and documentation update, ensuring
  you also update the `CHANGELOG.md` file with the relevant date.

* Create the new release with, this will create a zip file, upload to CDN and
  release the new documentation in one hit.

      grunt prep-release jcu-publish

  If there are any final changes to be committed, commit them and publish the
  docs pages again with:

      grunt buildcontrol:pages

* Tag the current commit with the given version number:

      git tag v1.0.0-beta.1
      git push --tags

* Push all remaining changes to GitHub after a final merge into `master`:

      git checkout master
      git merge -s recursive -X theirs develop
      git push origin master develop

* Now upload the final zip file to GitHub in the releases area, typing in the
  given tag version, publish the release and you are done!

## Cleaning up the CDN

If old directories need to be cleaned up on the CDN, use the following `rsync`
command.  This includes only the given directory (`dir_to_delete`) and its
contents inside the given target location on the CDN.

~~~ shell
rsync -arv --delete --include='/dir_to_delete/***' --exclude='*' $(mktemp -d)/ jcu0@rsync.keycdn.com:zones/jcu/
~~~
