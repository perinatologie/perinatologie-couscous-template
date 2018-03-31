---
id: home
---
# perinatologie.nl couscous template

## Introduction

Documentation on perinatologie.nl is written in markdown, version controlled on github, and published to static HTML through [couscous](http://couscous.io/).

This repository contains a reusable template for perinatologie.nl documentation

* [couscous.io](http://couscous.io)
* [couscous getting started](http://couscous.io/docs/getting-started.html)

## Usage in external documents

To use the template, set it up in your `couscous.yml` configuration file:

```yaml
template:
    url: https://github.com/perinatologie/perinatologie-couscous-template
```

## Configuration

Here are all the variables you can set in your `couscous.yml`:

```yaml
# Base URL of the published website
baseUrl: http://username.github.io/project

# Used to link to the GitHub project
github:
    user: myself
    repo: my-project

title: My project
subTitle: This is a great project.

# The left menu bar
menu:
    items:
        home:
            text: Home page
            # You can use relative urls
            relativeUrl: doc/faq.html
        foo:
            text: Another link
            # Or absolute urls
            absoluteUrl: https://example.com
```

Note that the menu items can also contain HTML:

```yaml
home:
    text: "<i class=\"fa fa-github\"></i> Home page"
    relativeUrl: doc/faq.html
```

## Menu

To set the current menu item (i.e. highlighted menu item), set the `currentMenu`
key in the Markdown files:

```markdown
---
currentMenu: home
---

# Welcome
```

## Preview

This template can be previewed inline. Simply install couscous, and run:

    couscous preview

Now point your browser to http://localhost:8000