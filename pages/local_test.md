---
layout: page
title: Testing your site locally
---

To test your site locally, you'll need

- [ruby](https://www.ruby-lang.org/en/)
- the [github-pages](https://github.com/github/pages-gem) gem

### Installing ruby

There are
[lots of different ways to install ruby](https://www.ruby-lang.org/en/installation/).


In Mac OS X, older versions of ruby will already be installed.  But I
use the [Ruby Version Manager (RVM)](http://rvm.io/) to have a more
recent version.  You could also use [Homebrew](http://brew.sh/).

In Windows, use [RubyInstaller](http://rubyinstaller.org/). (In most
of this tutorial, I've assumed you're using a Mac or some flavor of
Unix. It's possible that none of this was usable for Windows
folks. Sorry!)


### Installing the github-pages gem

Run the following command:

    gem install github-pages

This will install the `github-pages` gem and all dependencies
(including [jekyll](http://jekyllrb.com/)).

Later, to update the gem, type:

    gem update github-pages


### Testing your site locally

To construct and test your site locally, go into the directory and
type

    jekyll build

This will create (or modify) a `_site/` directory, containing
everything from `assets/`, and then the `index.md` and all
`pages/*.md` files, converted to html. (So there'll be
`_site/index.html` and the various `_site/pages/*.html`.)

Type the following in order to &ldquo;serve&rdquo; the site.

    jekyll serve

Now open your browser and go to
[http://localhost:4000](http://localhost:4000)
