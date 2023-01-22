# Landing Page Jekyll

Quickly generate landing pages to PoC new ideas

### [Live demo](https://mikeqdev.github.io/landing-page-gen-jekyll/)

## Quick Start

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

## Developing

Note: Do not modify `./_site/`, as this directory contains the generated HTML file(s)

### Content CRUD

Update \*.md files in `./stuff/`. Ensure to specify a `weight` for proper ordering

### Styling

Update in `./_sass/`, then update in `./assets/` if needed

### Images

Add images to `./assets/`, then reference them in your markdown files

## Todo

- Add usage notes and examples
- Linting and formatting?
- Should Ruby be upgraded?
- Analytics?
- Reusable 'theme'? Versioning?
