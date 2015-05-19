Web API Docs
============

[Slate ReadMe](https://github.com/tripit/slate)

[![Build Status](https://travis-ci.org/tripit/slate.svg?branch=master)](https://travis-ci.org/tripit/slate) [![Dependency Status](https://gemnasium.com/tripit/slate.png)](https://gemnasium.com/tripit/slate)

Slate helps you create beautiful API documentation. Think of it as an intelligent, responsive documentation template for your API.

<img src="https://dl.dropboxusercontent.com/u/95847291/github%20images/slate/slate_screenshot_new.png" width=700 alt="Screenshot of Example Documentation created with Slate">

*The example above was created with Slate. Check it out at [tripit.github.io/slate](http://tripit.github.io/slate).*

Slate Workflow
--------------

1. Make changes on `master` mainly to `source/index.md` or `includes/`
2. Commit and push yo' codez
3. Make sure you have checked out `gh-pages` branch
4. On `master` run `rake publish`

Getting Started with Slate
------------------------------

### Prerequisites

You're going to need:

 - **Linux or OS X** — Windows may work, but is unsupported.
 - **Ruby, version 1.9.3 or newer**
 - **Bundler** — If Ruby is already installed, but the `bundle` command doesn't work, just run `gem install bundler` in a terminal.

### Getting Set Up

 1. Fork this repository on Github.
 2. Clone *your forked repository* (not our original one) to your hard drive with `git clone https://github.com/YOURUSERNAME/slate.git`
 3. `cd slate`
 4. Install all dependencies: `bundle install`
 5. Start the test server: `bundle exec middleman server`

Or use the included Dockerfile! (must install Docker first)

```shell
docker build -t slate .
docker run -d -p 4567:4567 slate
```

You can now see the docs at <http://localhost:4567>. Whoa! That was fast!

*Note: if you're using the Docker setup on OSX, the docs will be
availalable at the output of `boot2docker ip` instead of `localhost:4567`.*

Now that Slate is all set up your machine, you'll probably want to learn more about [editing Slate markdown](https://github.com/tripit/slate/wiki/Markdown-Syntax), or [how to publish your docs](https://github.com/tripit/slate/wiki/Deploying-Slate).
