# Landing Page Jekyll

Quickly generate landing pages to PoC new ideas

### [Live demo](https://mikeqdev.github.io/landing-page-gen-jekyll/)

## Quick Start

### Using this theme

`jekyll new mySite`

Update `Gemfile`
- Remove any default themes (e.g.: `minima`)
- Add `gem "jekyll-remote-theme"` to support loading theme from GitHub

Update `_config.yml`
- Add `jekyll-remote-theme` to `plugins` list
- Replace any existing theme with `remote_theme: mikeqdev/landing-page-gen-jekyll@<release-version>`
- Add `collections: [ stuff ]`
  - _Skipping this step will result in error: `Cannot sort a null object.`_

Update `index.md` (the `dualpane.html` file will iterate over `site.stuff` from the `_config.yml`, which points to `_stuff` dir in next step)
```
---
layout: default
---
{% include dualpane.html %}
```

Create a `_stuff` directory and add content there. Check examples in [_stuff](_stuff) for reference
- _Skipping this step will result in no content on your page. Also, check the page source in your browser to further troubleshoot_

Install dependencies: `bundler install`

Serve locally: `bundler exec jekyll serve`

### Developing this theme

Ruby 2.5 --> `gem install bundler -v 2.3.14`

```
bundle install
```

To start the Jekyll local development server.

```
bundle exec jekyll serve [--host=0.0.0.0]
```

To build the site. Output goes to `./_site/`.

```
bundle exec jekyll build
```

To make available to consumers, create a release (with tag) in GitHub. Consumers can then specify version in `jekyll-remote-theme` (or via branch name)

To publish to gh-page (see [Live demo](https://mikeqdev.github.io/landing-page-gen-jekyll/)), simply push to `gh-pages` branch

#### Structure

Note: Do not modify `./_site/`, as this directory contains the generated HTML file(s)

##### Content CRUD

Update \*.md files in `./_stuff/`. Ensure to specify a `weight` for proper ordering

##### Styling

Update in `./_sass/`, then update in `./assets/` if needed

##### Images

Add images to `./assets/`, then reference them in your markdown files

## Todo

- Add usage notes and examples
- Linting and formatting?
- Should Ruby be upgraded?
- Analytics?
- Reusable 'theme'? Versioning?
- SEO tag plugin?
